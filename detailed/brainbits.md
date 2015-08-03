# BrainBits

BrainBits is a tool to organise my brain. I want to have something that brings computing closer to how i think about stuff. Stuff like notes, todos, documents, code, projects, bookmarks, research, articles i want to read… I want to have this information available to me in the shortest possible time and i want an interface that is as simple as possible. I also want it to be super light so that i can deploy it fast and use it fast. Having it in the cloud and thus being able to access all my stuff from anywhere is also nice.

The basic idea is that all this information is pretty much the same: A title, a body, tags and other metadata.

All the other stuff follows from there:

	- Documents are notes exported to latex (through MMD) #file
	- Projects are smart tag collections (Boolean: @foo @bar !@baz)
	- Contexts for tasks are @tags
	- bookmarks are a note with a "title" and a url (in the body) and eventual note. whatever. #bookmark
	- read it later articles are the same but with a #rl tag (plus #rl collection).  they are displayed uncluttered. can #rl tag to any #file to display it uncluttered (with readability API by default) (rendered view not editable). Can have other tags and can have #read({date}) tag. whatever

It seems to me that a lot of things could be stored (and displayed) in this format:

	- thoughts, notes & memos
	- emails
	- wiki 
	- blog entries (through mint)
	- wiki entries (BrainBits are cross linkable) (through mint)
	- dissertations or long and complex documents (through outliner and latex export)
	- Read later entry
	- microblog entry (through mint)
	- Collaborative doc editing with GIT and LaTeX (through collaborator)
	- code
		- SVG (through Designer)
		- HTML
		- any markup
		- CSS
		- proxy folder structure can be represented by tags (/foo/bar/baz).
		- Dropbox integration for all /tags

All these things are BrainBits. A BrainBit is simply an entry with a title, a body and tags (plus some other info like 'date created' ). It's essentially very similar to a plain text file.

PS: Attachments are simply URLs coded into MMD. Tools should be provided to simplify the task (e.g. insert image, file etc), no images or files are hosted on BrainBits (Keeps my server happy through services like cloud.app and picasa)

## Structure:

A BrainBit is stored as an entry in the BrainBits db table 

BrainBit has:

	one:
	- title
	- date created
	- date modified
	- file_type (.md by default but can do .html .css .tex etc.)
	many:
	- tags
		
User has:
	
	one:
	- uname
	- password
	- email
	many:
	- tags
	- connections
	
User's Connection has:

	many:
	- tags (eg. home, work, school .. a la circles in G+)

## Interface

	[N] [T] || inbox || collections || browse ||       <-->      @ || [ search...  ]

That's it. That's the toolbar. It is always visible at the top of the screen but can auto-hide (and be pinned) in fullscreen

	[N] = new note (@note); if already editing a note, open in lightbox mode 
	[T] = new task (@task); if already editing a note, open in lightbox mode
	inbox = untagged stuff goes here
	collections = (smart) collections a la Punakea, but also support for  BOOL searches on tags & dates 
	browse = details view a la nvALT. inline editing and batch editing for both tags and titles. ajax action going for autocompletion please. Views a la Pocket.app
	
	@ = opens drawer with tag cloud in inbox, browse and search. Acts as tag picker for making collections. Tag editor for new entry or new note
	
	search = searches your BrainBits :)
	
Notes and tasks are differentiated with colour

## Documentation

These things should be documented, so that anyone can learn 'em:

	- MMD
	- tags
	- downloading & converting to latex
	- publishing

## MISC
	- Alfred integration
	- nvALT integration
	- download to archive (keep my server happy)
	- open software platform that anyone can deploy
	- OpenID
	- can email link to BrainBit or tweet about a BrainBit or mint a BrainBit (Mints)
	- can link notes to each other (wiki)
	- supertags? @gla @batch
	- local storage (HTML5)
	- task editor?
	- LaTex export

# Companion apps

## Tasker
Edits tasks a la TaskPaper? how?

## autoicons
Assigns icons to tags

## Textexpander
through js + snippet market
 
## Outliner
sidebar for tags with doc outline (MMD). Can rearrange sections and view a la scrivener
					
## Collaborator
GIT for collaboration on notes (Docs)

## Designer
 graphic interface to edit SVG files

## Coder
text editor with syntax support

## Mint
latex export for BrainBits or any MMD text
	
## BrainStream

Blog like platform, to publish BrainBits
Integrated in BrainBits.
button in tags "publish". shows if 'local' version is different than published one

### Interface
	home ||  	  <--> 		@ || [  search...   ] 
	
		home = page that can be configured by user. What tags does it display? format?
		search = 
		@ = opens tag cloud lightbox
### Structure

BrainStream has:

	one:
	- theme
	- user? (collaboration?)

BrainStrem has:

	one:
	- BrainBit
	many:
	- +1s
	
## Stream
Choose  tags and view relevant mints

	___________________________________
				STREAM
				Choose some @
	___________________________________
	
					[tagcloud, mixed with BrainBit previews]
					
	____________________________________