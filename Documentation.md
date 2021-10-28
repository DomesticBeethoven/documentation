<!-----
Conversion notes:

* Docs to Markdown version 1.0β31
* Wed Oct 27 2021 13:40:48 GMT-0700 (PDT)
* Source doc: Documentation v.2
----->
October 2021


# Beethoven in the House: Model documentation

This document provides an overview of the organisation of our structural model as detailed in the Beethoven in the House “[Core Concept Documentation](https://docs.google.com/document/d/1li0TX6RPYoCmr0ZqM24I6PYZcpjc-rL96rx0lLYV2C4/edit?usp=sharing)”.


[Model](#heading=h.6hhynxdf5wtq)



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "1. Evidence objects"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[1. Evidence objects](#heading=h.quhpm5izeinj)

	[Resources](#bookmark=id.8f6laplxwf4t)

	[References](#bookmark=id.dd160n2gval2)



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "2. Musical objects"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[2. Musical objects](#heading=h.8zgtsgm1emj7)

	[Selection](#bookmark=id.y335anir1t44)

	[Extract](#bookmark=id.t3vbgs6wx6q7)

	[Musical Material](#bookmark=id.deurz458gwic)

	[Musical Idea](#bookmark=id.r4z5yln2cx5q)



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "3. Musicological objects"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[3. Musicological objects](#heading=h.b2zx3u2rk1dk)

	[Observation](#bookmark=id.v7c4cq1kr137)

	[Relationship](#bookmark=id.3z1vu4kcelm2)

	[Commentary](#bookmark=id.prvw4ky6721h)


# MODEL

We present here our original conception of a multi-layered hierarchy and describe how we propose to operationalize these concepts in order to provide a framework for musical annotation. Briefly stated, this model shows how portions of digitized data in various files and formats can be identified, selected, labelled, and compared.

The following chart presents a top-down view.

NIRVANA-ED STACK MODEL

Each layer corresponds to one of the three main categories of objects that represent our data: raw materials and digitized sources; user-selected musical elements and their aggregates in various relevant combinations; and their musicological labellying and scholarly commentary.

Preliminary to the primary scholarly activity, which is research commentary involving multiple sources, there is a series of steps that must be completed: identification of available resources, selection of items of interest and pulling out reference IDs, among others. The two lower levels of the model are then, generally speaking, concerned with collecting the desired data, while the upper level involves critical judgement.

A bottom-up overview of the structures is presented below. ~~The entities described align closely with FRBR entities, and FRBR terminology is used whenever possible.~~



1. EVIDENCE OBJECTS

These are digitized materials that will be used for the musicological investigation. This includes the images of musical scores and the MEI encodings that are stored on the project repository. It also includes music recordings (in the form of audio files, digital video, image files), text documents, and URIs of secondary source materials, such as books and articles.

**<code><span style="text-decoration:underline;">Resources</span></code></strong> refer to complete documents or files we have access to.

**Examples**



* a MEI file: [https://github.com/DomesticBeethoven/data/blob/main/op.%2093/QuintettSteiner%20-%20D-BNba%20C93_26/D-BNba93_26.1st.36-44.mei](https://github.com/DomesticBeethoven/data/blob/main/op.%2093/QuintettSteiner%20-%20D-BNba%20C93_26/D-BNba93_26.1st.36-44.mei)
* a IIIF image: [https://github.com/DomesticBeethoven/api/Scaler/IIIF/C93-26/…](https://github.com/DomesticBeethoven/api/Scaler/IIIF/C93-26/…)
* a MP3 file: [https://github.com/DomesticBeethoven/api/audio/MackerrasLvbOp93.mp3](https://github.com/DomesticBeethoven/api/audio/MackerrasLvbOp93.mp3)
* a PDF document: [https://doi.org/10.2307/763996](https://doi.org/10.2307/763996)

**<code><span style="text-decoration:underline;">References</span></code></strong> are the URIs used to retrieve the <code>Resources</code> or to point to a place or region in the <code>Resources</code>.

 \
**Examples**



* the xml:id of an MEI note or measure element: #D-BNba93_26.1st.36-44.mei#measure_36
* an element that contains cardinal coordinates on an image facsimile: &lt;**graphic** xml:id="graphic_f6fde83d-64" target="00030.jpg" type="facsimile" width="3240" height="4030"/>&lt;**zone** xml:id="zone_c564dbd0-0d" type="measure" ulx="314" uly="460" lrx="1164" lry="776"/>
* a timestamp: MackerrasLvbOp93.mp3#t45-60
* a DOI: doi:10.2307/746230



2.
MUSICAL OBJECTS
These refer to the proper music that will be investigated, be it in whole or in part, in notated, image, audio or video format. The types of musical objects remit to the various levels of collection and abstraction of the research object and align closely with FRBR entities. FRBR terminology is then used whenever possible, although there are particularities pertaining to the domain of music that will be taken into consideration. Any of the musical objects may be the target of a musicological object.

~~Between the level of individual reference IDs and musically meaningful portions of the music is the **<code><span style="text-decoration:underline;">Selection</span></code></strong>. </del>

A **<code><span style="text-decoration:underline;">Selection</span></code></strong> is <del>a purely functional entity</del> the lowest level of grouping musical references. It contains the complete set of URIs for the individual components of a musical extract, be it in a single or in multiple resources that belong to an unique source material. It is comparable to frbr:Manifestation in the sense that it gathers digitized embodiments of a piece. Every <code>Selection</code> must be part of an <code>Extract</code>.

**Examples**



* an area on the surface of the score
* part of a music audio/video file
* a section of a scanned letter
* a passage in the instrumental parts of the same musical score

An **<code><span style="text-decoration:underline;">Extract</span></code></strong> collects various instances of a feature we want to identify and comprises single or multiples frbr:Manifestation of an unique musical expression <del>and is the minimum level that can be the target of an annotation</del>. In other words, it is used to combine <code>Selections</code> of different source materials.

**Examples**



* an area on the surface of the score
* part of a music audio/video file
* a section of a scanned letter
* a combination of selections from different sources, such as the xml:ids of consecutive measures in an MEI file and the timestamps of its corresponding section in an audio file

**<code><span style="text-decoration:underline;">MusicalMaterial</span></code></strong> is an abstract entity that refers to the musical concept behind a music extract, such as a passage, phrase or fragment. It is primarily used to <del>compare</del> group a particular aspect of a musical extract with an analogous, or what we are calling a <em>parallel</em> moment or passage in distinct versions of a musical work?piece?. <code>MusicalMaterial</code> represents a communal musical thought, independent of its various manifestations in different arrangements or recordings (or, in a variation set, within a single variation).

Since it is an abstraction, `MusicalMaterial` is also subjective, and does not necessarily have a notated expression. It can correspond to just a “core” musical thought or be identical with one of its expressions, according to the user’s interpretation of the music.  Another relevant aspect of `MusicalMaterial` is that it can refer to any segment of music, independent of formal structures. It can be compared to a frbr:Expression because it represents the realization of a `MusicalIdeal`.

**Examples**



* the recapitulation section in two arrangements of the same work
* a citation from a piece that is featured in another piece: the Dies Irae theme in the 4th movement of Berlioz’s _Symphonie fantastique_
* the variations of _La Folia_ in view of its manifestations within a single piece

**<code><span style="text-decoration:underline;">MusicalIdea</span></code></strong> is an abstract entity that refers to the musical thought behind a recurring musical structure, such as a theme or a motiv. Although it is similar to <code>MusicalMaterial</code> in the sense that it is an abstraction, <code>MusicalIdea</code> primarily expresses elements that are reused within a single musical piece, and consequently has greater affinity with established musical structures. As  <code>MusicalMaterial</code>, <code>MusicalIdea</code> is a subjective matter and does not require a notated form. It may also be comparable to a frbr:Work in the sense that it is an idealized “seed” of its multiple expressions throughout a musical piece.

The various instances of recurring musical structures, which can be stored in `Selections`, `Extracts` or `MusicalMaterials`, are collected then in the `MusicalIdea`.

**Examples**



* the entries of a subject in a fugue
* a motiv that is repeated and developed in a sonata-form piece
* the statement of  _La Folia_‘s theme in different variations set



3.
MUSICOLOGICAL OBJECTS
Here is where the musicological research takes place _per se_. These objects are used to describe, compare and record historical information on the collected musical objects, as well as to present hypotheses, link them to non-musical sources and make scholarly commentary. All this is accomplished through the formalized structure of the web annotation, thus preserving their motivation and provenance.

**<code><span style="text-decoration:underline;">Observations</span></code></strong> usually contain a simple textual remark that targets a musical object. In most cases, it will be used to label such objects or to present one of their relevant features. <code>Observations</code> aim to be (relatively) objective, non-controversial, or traditional descriptions, so that they can be reused.

**Examples**



* a label: “This is the theme A of this sonata-form movement.”
* something notable: “There is a _fff_ (fortississimo) marking here.”
* a description; “The development section starts with bassoon and oboe playing the main motiv.”

**<code><span style="text-decoration:underline;">Relationships</span></code></strong> is used to juxtapose more than one musical object by connecting <code>Observations</code>, <code>Commentaries</code> and other <code>Relationships</code>. They also aim to be a simple text remark, usually noting a commonality, a transformation, an addition or a deletion between <code>Observations</code>. More complex details, such as the reason for a particular change, are recorded in <code>Commentaries</code>.

**Examples**



* a comparison: “The _fff_ (fortississimo) marking in version A was substituted by an _ff_ (fortissimo) in version B.”
* noting a common pattern: “The  _fff_ to _ff_ substitution occurs in these three passages.”
* a deletion: “The introduction was suppressed in version B.”

**<code><span style="text-decoration:underline;">Commentaries</span></code></strong> are used to make more complex comparisons, bring attention to relevant aspects of the music and to present hypotheses, among others. <code>Commentaries</code> can also present historical or analytical reflections informed by academic research, including pointing out to external sources and references.

**Examples**



* a comparison: “.”
* a notable event: “At this time, _fff_ markings were absolutely rare. They were probably introduced in the musical vocabulary by Beethoven himself, and even then they figure only in three of his works (see SHEER 1998, 361).
* a hypothesis: “This substitution may have been done due to the change in instrumentation.”
