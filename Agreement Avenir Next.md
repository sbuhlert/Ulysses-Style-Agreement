// **Agreement Style** for Ulysses
//
// © Steffen Buhlert (2018) under the GNU General Public License version 3
// https://opensource.org/licenses/GPL-3.0
//
// suitable for contracts and other legal documents etc.
// heading-6 to be used for recital definitions
//
// body and header font:		Avenir Next
// code font:		IBM Plex Mono
//
// heading-1: 		centered
// heading-5: 		centered
// heading-6: 		right aligned
//
// page numbers: 	bottom, centered
// footnotes: 		continuous


// Document & Layout Settings

document-settings {
page-inset-top:    30mm;	page-inset-inner:  30mm
page-inset-bottom: 30mm;	page-inset-outer:  30mm

	two-sided:		no
	page-binding:	left

	page-number-format:	"- %p -"
	page-number-style:	decimal

	footnote-enumeration:	continuous
	footnote-placement:		end-of-page
	footnote-style:			decimal

	}

area-footer {
    bottom-spacing:	1 cm
    content:         page-number
    text-alignment:  center
}

// Default Typography
// Avenir Next

defaults {

	font-family:	"Avenir Next"
	font-size:		11pt
	line-height:	14pt

	text-alignment: justified
	hyphenation:	yes

	}


// Basic Non-Text-Area Page Layout

area-header {

	font-family:	"Avenir Next"
	content:			none
	top-spacing:		12.5mm
	bottom-spacing:		0mm
	text-alignment: 	center

	}

area-footer {

	content:			page-number
	text-alignment: 	center

	}


area-footnotes {

	font-size:			9pt
	line-height:		12pt

	top-spacing:		10mm

	}


// Reusable styles (variables & mixins)

$mark-color =		#FEFECC
$black =			#000000
$light-grey =		#cccccc
$cool-blue = 		#3875d7


@code {

	font-family:	"IBM Plex Mono"
	font-weight:	normal;
	font-slant:		normal;
	font-size:		11pt

	}


// Headers

heading-all {
	font-family:	"Avenir Next"

	line-height:			125%;

	keep-with-following:	true

	}


heading-1 {

	style-title:	"Heading 1"
	// As shown and used by MS Word

	font-size:		14pt
	font-weight:	bold
	text-alignment:	center

	margin-top:		13pt

	margin-bottom:	6.5pt

	}


heading-2 {

	style-title:	"Heading 2"
	// As shown and used by MS Word

	font-size:		13pt
	font-weight:	bold
	text-alignment:	left

	margin-top:  	 13pt
	margin-bottom: 6.5pt

	}


heading-3 {

	style-title:	"Heading 3"
	// As shown and used by MS Word

	font-size:		12pt
	font-weight:	bold
	text-alignment:	left

	margin-top: 	 13pt;
	margin-bottom: 6.5pt

	}


heading-4 {

	style-title:	"Heading 4"
	// As shown and used by MS Word

	font-size:		12pt

	margin-top: 	 6.5pt;
	margin-bottom: 6.5pt

	}


heading-5 {

	style-title:	"Heading 5"
	// As shown and used by MS Word — but centered

	font-size:		11pt
	font-weight:	normal
	text-alignment:	center

	margin-top: 	 6.5pt;
	margin-bottom: 6.5pt

	}


heading-6 {

	style-title:	"Heading 6"
	// As shown and used by MS Word — but right alignment

	font-size:		11pt
	font-weight:	normal
	text-alignment:	right

	margin-top: 	 6.5pt;
	margin-bottom: 6.5pt

	}


// Paragraph styles

paragraph {

	style-title:		"Paragraph"
	// As shown and used by MS Word
	margin-bottom: 6.5pt

	}


paragraph-divider {

	page-break:			after
	// Set the divider to help with manual page breaks

	}


paragraph-figure {

	margin-top:		12pt
	margin-bottom:	12pt

	text-alignment:	center

}

paragraph + paragraph {
}


// Block styles

block-all {

	margin-top:		12pt
	margin-bottom:	12pt

	margin-left:	3em
	margin-right:	3em

	}


block-code : @code {

	style-title:	"Codeblock"
	// As shown and used by MS Word

	font-size:		11pt
	font-color:		$cool-blue
	line-height:	18pt

	margin-bottom:  18pt

	}


block-code paragraph {

	text-alignment:		left
	first-line-indent:	0pt

	hyphenation:		no

	default-tab-interval: 6em
	// Set tab stops

	}

block-quote {

	style-title:	"Blockquote"
	// As shown and used by MS Word

	font-slant:		italic

	margin-left: 	0em

	}


block-raw {

	visibility:	hidden
	// kills raw source blocks

	}


block-comment {

	visibility:	hidden

}


// List styles


list-all {

	margin-left:	2em
	margin-top:		6pt;

	}


list-all list-all {

	margin-top:		0pt;
	margin-bottom:	0pt;
	// No extra spacings between nested ordered and unordered lists

	}


list-ordered {

	enumeration-format:	"%d."
	text-inset:	1.5em;
	// Simulates tab stop justified right

	}


list-ordered list-ordered {

	enumeration-format:	"%*%d"
	text-inset:	2.2em;
	// Simulates tab stop justified right

	}


list-ordered list-ordered list-ordered {

	enumeration-format:	"%*.%d"
	text-inset:	2.9em;
	// Simulates tab stop justified right

	}


list-unordered {

	enumeration-format:	"-"
	text-inset:	1.5em;
	// Simulates tab stop justified right

	}


// Inline styles

inline-strong {

	style-title:	"Strong"
	// As shown and used by MS Word

	font-weight:	bold

	}


inline-emphasis {

	style-title:	"Emphasis"
	// As shown and used by MS Word

	font-slant: 	italic;

	}


inline-mark {

	style-title:		"Mark"
	// As shown and used by MS Word

	background-color:	$mark-color

	}


inline-citation {

	style-title:	"Inline Cite"
	// As shown and used by MS Word

	font-slant:		italic;

	}


inline-code : @code {

	style-title:	"Inline Code"
	// As shown and used by MS Word

	// Nothing else to set here, since it inherits from @code

	}


inline-link {

	style-title:		"Link"
	// As shown and used by MS Word

	font-color:	$cool-blue
	underline:	single
	underline-color: $cool-blue

	}


inline-comment {

	visibility:	hidden;
	// kills comments

	}


inline-delete {

	visibility:	hidden;
	// deletes deletions

	}


inline-annotation {

	background-color:	$mark-color

	}


inline-annotation:anchor {

	background-color:	#ffffff

	}


inline-raw {

	visibility:	hidden;
	// kills raw source

	}


//
// Ulysses specific stuff
// By default, we are hiding tags (##) etc.
//

ulysses-tag {

	visibility:	hidden

	}


inline-link ulysses-tag {

	visibility: hidden

	}


list-all ulysses-tag {

	visibility: hidden

	}
