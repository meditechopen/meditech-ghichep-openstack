<!DOCTYPE html>
<html>
  <head>
      <meta charset="utf-8" />
      <title>Markdown to HTML</title>
      <style>.markdown-preview:not([data-use-github-style]) { padding: 2em; font-size: 1.2em; color: rgb(171, 178, 191); overflow: auto; background-color: rgb(40, 44, 52); }
.markdown-preview:not([data-use-github-style]) > :first-child { margin-top: 0px; }
.markdown-preview:not([data-use-github-style]) h1, .markdown-preview:not([data-use-github-style]) h2, .markdown-preview:not([data-use-github-style]) h3, .markdown-preview:not([data-use-github-style]) h4, .markdown-preview:not([data-use-github-style]) h5, .markdown-preview:not([data-use-github-style]) h6 { line-height: 1.2; margin-top: 1.5em; margin-bottom: 0.5em; color: rgb(255, 255, 255); }
.markdown-preview:not([data-use-github-style]) h1 { font-size: 2.4em; font-weight: 300; }
.markdown-preview:not([data-use-github-style]) h2 { font-size: 1.8em; font-weight: 400; }
.markdown-preview:not([data-use-github-style]) h3 { font-size: 1.5em; font-weight: 500; }
.markdown-preview:not([data-use-github-style]) h4 { font-size: 1.2em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) h5 { font-size: 1.1em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) h6 { font-size: 1em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) strong { color: rgb(255, 255, 255); }
.markdown-preview:not([data-use-github-style]) del { color: rgb(124, 135, 156); }
.markdown-preview:not([data-use-github-style]) a, .markdown-preview:not([data-use-github-style]) a code { color: rgb(82, 139, 255); }
.markdown-preview:not([data-use-github-style]) img { max-width: 100%; }
.markdown-preview:not([data-use-github-style]) > p { margin-top: 0px; margin-bottom: 1.5em; }
.markdown-preview:not([data-use-github-style]) > ul, .markdown-preview:not([data-use-github-style]) > ol { margin-bottom: 1.5em; }
.markdown-preview:not([data-use-github-style]) blockquote { margin: 1.5em 0px; font-size: inherit; color: rgb(124, 135, 156); border-color: rgb(75, 83, 98); border-width: 4px; }
.markdown-preview:not([data-use-github-style]) hr { margin: 3em 0px; border-top: 2px dashed rgb(75, 83, 98); background: none; }
.markdown-preview:not([data-use-github-style]) table { margin: 1.5em 0px; }
.markdown-preview:not([data-use-github-style]) th { color: rgb(255, 255, 255); }
.markdown-preview:not([data-use-github-style]) th, .markdown-preview:not([data-use-github-style]) td { padding: 0.66em 1em; border: 1px solid rgb(75, 83, 98); }
.markdown-preview:not([data-use-github-style]) code { color: rgb(255, 255, 255); background-color: rgb(58, 63, 75); }
.markdown-preview:not([data-use-github-style]) pre.editor-colors { margin: 1.5em 0px; padding: 1em; font-size: 0.92em; border-radius: 3px; background-color: rgb(49, 54, 63); }
.markdown-preview:not([data-use-github-style]) kbd { color: rgb(255, 255, 255); border-width: 1px 1px 2px; border-style: solid; border-color: rgb(75, 83, 98) rgb(75, 83, 98) rgb(62, 68, 81); background-color: rgb(58, 63, 75); }
.markdown-preview[data-use-github-style] { font-family: "Helvetica Neue", Helvetica, "Segoe UI", Arial, freesans, sans-serif; line-height: 1.6; word-wrap: break-word; padding: 30px; font-size: 16px; color: rgb(51, 51, 51); overflow: scroll; background-color: rgb(255, 255, 255); }
.markdown-preview[data-use-github-style] > :first-child { margin-top: 0px !important; }
.markdown-preview[data-use-github-style] > :last-child { margin-bottom: 0px !important; }
.markdown-preview[data-use-github-style] a:not([href]) { color: inherit; text-decoration: none; }
.markdown-preview[data-use-github-style] .absent { color: rgb(204, 0, 0); }
.markdown-preview[data-use-github-style] .anchor { position: absolute; top: 0px; left: 0px; display: block; padding-right: 6px; padding-left: 30px; margin-left: -30px; }
.markdown-preview[data-use-github-style] .anchor:focus { outline: none; }
.markdown-preview[data-use-github-style] h1, .markdown-preview[data-use-github-style] h2, .markdown-preview[data-use-github-style] h3, .markdown-preview[data-use-github-style] h4, .markdown-preview[data-use-github-style] h5, .markdown-preview[data-use-github-style] h6 { position: relative; margin-top: 1em; margin-bottom: 16px; font-weight: bold; line-height: 1.4; }
.markdown-preview[data-use-github-style] h1 .octicon-link, .markdown-preview[data-use-github-style] h2 .octicon-link, .markdown-preview[data-use-github-style] h3 .octicon-link, .markdown-preview[data-use-github-style] h4 .octicon-link, .markdown-preview[data-use-github-style] h5 .octicon-link, .markdown-preview[data-use-github-style] h6 .octicon-link { display: none; color: rgb(0, 0, 0); vertical-align: middle; }
.markdown-preview[data-use-github-style] h1:hover .anchor, .markdown-preview[data-use-github-style] h2:hover .anchor, .markdown-preview[data-use-github-style] h3:hover .anchor, .markdown-preview[data-use-github-style] h4:hover .anchor, .markdown-preview[data-use-github-style] h5:hover .anchor, .markdown-preview[data-use-github-style] h6:hover .anchor { padding-left: 8px; margin-left: -30px; text-decoration: none; }
.markdown-preview[data-use-github-style] h1:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h2:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h3:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h4:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h5:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h6:hover .anchor .octicon-link { display: inline-block; }
.markdown-preview[data-use-github-style] h1 tt, .markdown-preview[data-use-github-style] h2 tt, .markdown-preview[data-use-github-style] h3 tt, .markdown-preview[data-use-github-style] h4 tt, .markdown-preview[data-use-github-style] h5 tt, .markdown-preview[data-use-github-style] h6 tt, .markdown-preview[data-use-github-style] h1 code, .markdown-preview[data-use-github-style] h2 code, .markdown-preview[data-use-github-style] h3 code, .markdown-preview[data-use-github-style] h4 code, .markdown-preview[data-use-github-style] h5 code, .markdown-preview[data-use-github-style] h6 code { font-size: inherit; }
.markdown-preview[data-use-github-style] h1 { padding-bottom: 0.3em; font-size: 2.25em; line-height: 1.2; border-bottom: 1px solid rgb(238, 238, 238); }
.markdown-preview[data-use-github-style] h1 .anchor { line-height: 1; }
.markdown-preview[data-use-github-style] h2 { padding-bottom: 0.3em; font-size: 1.75em; line-height: 1.225; border-bottom: 1px solid rgb(238, 238, 238); }
.markdown-preview[data-use-github-style] h2 .anchor { line-height: 1; }
.markdown-preview[data-use-github-style] h3 { font-size: 1.5em; line-height: 1.43; }
.markdown-preview[data-use-github-style] h3 .anchor { line-height: 1.2; }
.markdown-preview[data-use-github-style] h4 { font-size: 1.25em; }
.markdown-preview[data-use-github-style] h4 .anchor { line-height: 1.2; }
.markdown-preview[data-use-github-style] h5 { font-size: 1em; }
.markdown-preview[data-use-github-style] h5 .anchor { line-height: 1.1; }
.markdown-preview[data-use-github-style] h6 { font-size: 1em; color: rgb(119, 119, 119); }
.markdown-preview[data-use-github-style] h6 .anchor { line-height: 1.1; }
.markdown-preview[data-use-github-style] p, .markdown-preview[data-use-github-style] blockquote, .markdown-preview[data-use-github-style] ul, .markdown-preview[data-use-github-style] ol, .markdown-preview[data-use-github-style] dl, .markdown-preview[data-use-github-style] table, .markdown-preview[data-use-github-style] pre { margin-top: 0px; margin-bottom: 16px; }
.markdown-preview[data-use-github-style] hr { height: 4px; padding: 0px; margin: 16px 0px; border: 0px none; background-color: rgb(231, 231, 231); }
.markdown-preview[data-use-github-style] ul, .markdown-preview[data-use-github-style] ol { padding-left: 2em; }
.markdown-preview[data-use-github-style] ul.no-list, .markdown-preview[data-use-github-style] ol.no-list { padding: 0px; list-style-type: none; }
.markdown-preview[data-use-github-style] ul ul, .markdown-preview[data-use-github-style] ul ol, .markdown-preview[data-use-github-style] ol ol, .markdown-preview[data-use-github-style] ol ul { margin-top: 0px; margin-bottom: 0px; }
.markdown-preview[data-use-github-style] li > p { margin-top: 16px; }
.markdown-preview[data-use-github-style] dl { padding: 0px; }
.markdown-preview[data-use-github-style] dl dt { padding: 0px; margin-top: 16px; font-size: 1em; font-style: italic; font-weight: bold; }
.markdown-preview[data-use-github-style] dl dd { padding: 0px 16px; margin-bottom: 16px; }
.markdown-preview[data-use-github-style] blockquote { padding: 0px 15px; color: rgb(119, 119, 119); border-left: 4px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] blockquote > :first-child { margin-top: 0px; }
.markdown-preview[data-use-github-style] blockquote > :last-child { margin-bottom: 0px; }
.markdown-preview[data-use-github-style] table { display: block; width: 100%; overflow: auto; word-break: keep-all; }
.markdown-preview[data-use-github-style] table th { font-weight: bold; }
.markdown-preview[data-use-github-style] table th, .markdown-preview[data-use-github-style] table td { padding: 6px 13px; border: 1px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] table tr { border-top: 1px solid rgb(204, 204, 204); background-color: rgb(255, 255, 255); }
.markdown-preview[data-use-github-style] table tr:nth-child(2n) { background-color: rgb(248, 248, 248); }
.markdown-preview[data-use-github-style] img { max-width: 100%; box-sizing: border-box; }
.markdown-preview[data-use-github-style] .emoji { max-width: none; }
.markdown-preview[data-use-github-style] span.frame { display: block; overflow: hidden; }
.markdown-preview[data-use-github-style] span.frame > span { display: block; float: left; width: auto; padding: 7px; margin: 13px 0px 0px; overflow: hidden; border: 1px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] span.frame span img { display: block; float: left; }
.markdown-preview[data-use-github-style] span.frame span span { display: block; padding: 5px 0px 0px; clear: both; color: rgb(51, 51, 51); }
.markdown-preview[data-use-github-style] span.align-center { display: block; overflow: hidden; clear: both; }
.markdown-preview[data-use-github-style] span.align-center > span { display: block; margin: 13px auto 0px; overflow: hidden; text-align: center; }
.markdown-preview[data-use-github-style] span.align-center span img { margin: 0px auto; text-align: center; }
.markdown-preview[data-use-github-style] span.align-right { display: block; overflow: hidden; clear: both; }
.markdown-preview[data-use-github-style] span.align-right > span { display: block; margin: 13px 0px 0px; overflow: hidden; text-align: right; }
.markdown-preview[data-use-github-style] span.align-right span img { margin: 0px; text-align: right; }
.markdown-preview[data-use-github-style] span.float-left { display: block; float: left; margin-right: 13px; overflow: hidden; }
.markdown-preview[data-use-github-style] span.float-left span { margin: 13px 0px 0px; }
.markdown-preview[data-use-github-style] span.float-right { display: block; float: right; margin-left: 13px; overflow: hidden; }
.markdown-preview[data-use-github-style] span.float-right > span { display: block; margin: 13px auto 0px; overflow: hidden; text-align: right; }
.markdown-preview[data-use-github-style] code, .markdown-preview[data-use-github-style] tt { padding: 0.2em 0px; margin: 0px; font-size: 85%; border-radius: 3px; background-color: rgba(0, 0, 0, 0.0392157); }
.markdown-preview[data-use-github-style] code::before, .markdown-preview[data-use-github-style] tt::before, .markdown-preview[data-use-github-style] code::after, .markdown-preview[data-use-github-style] tt::after { letter-spacing: -0.2em; content: " "; }
.markdown-preview[data-use-github-style] code br, .markdown-preview[data-use-github-style] tt br { display: none; }
.markdown-preview[data-use-github-style] del code { text-decoration: inherit; }
.markdown-preview[data-use-github-style] pre > code { padding: 0px; margin: 0px; font-size: 100%; word-break: normal; white-space: pre; border: 0px; background: transparent; }
.markdown-preview[data-use-github-style] .highlight { margin-bottom: 16px; }
.markdown-preview[data-use-github-style] .highlight pre, .markdown-preview[data-use-github-style] pre { padding: 16px; overflow: auto; font-size: 85%; line-height: 1.45; border-radius: 3px; background-color: rgb(247, 247, 247); }
.markdown-preview[data-use-github-style] .highlight pre { margin-bottom: 0px; word-break: normal; }
.markdown-preview[data-use-github-style] pre { word-wrap: normal; }
.markdown-preview[data-use-github-style] pre code, .markdown-preview[data-use-github-style] pre tt { display: inline; max-width: initial; padding: 0px; margin: 0px; overflow: initial; line-height: inherit; word-wrap: normal; border: 0px; background-color: transparent; }
.markdown-preview[data-use-github-style] pre code::before, .markdown-preview[data-use-github-style] pre tt::before, .markdown-preview[data-use-github-style] pre code::after, .markdown-preview[data-use-github-style] pre tt::after { content: normal; }
.markdown-preview[data-use-github-style] kbd { display: inline-block; padding: 3px 5px; font-size: 11px; line-height: 10px; color: rgb(85, 85, 85); vertical-align: middle; border-width: 1px; border-style: solid; border-color: rgb(204, 204, 204) rgb(204, 204, 204) rgb(187, 187, 187); border-radius: 3px; box-shadow: rgb(187, 187, 187) 0px -1px 0px inset; background-color: rgb(252, 252, 252); }
.markdown-preview[data-use-github-style] a { color: rgb(51, 122, 183); }
.markdown-preview[data-use-github-style] code { color: inherit; }
.markdown-preview[data-use-github-style] pre.editor-colors { padding: 0.8em 1em; margin-bottom: 1em; font-size: 0.85em; border-radius: 4px; overflow: auto; }
.scrollbars-visible-always .markdown-preview pre.editor-colors .vertical-scrollbar, .scrollbars-visible-always .markdown-preview pre.editor-colors .horizontal-scrollbar { visibility: hidden; }
.scrollbars-visible-always .markdown-preview pre.editor-colors:hover .vertical-scrollbar, .scrollbars-visible-always .markdown-preview pre.editor-colors:hover .horizontal-scrollbar { visibility: visible; }
.markdown-preview .task-list-item-checkbox { position: absolute; margin: 0.25em 0px 0px -1.4em; }
.bracket-matcher .region {
  border-bottom: 1px dotted lime;
  position: absolute;
}

.spell-check-misspelling .region {
  border-bottom: 2px dotted rgba(255, 51, 51, 0.75);
}
.spell-check-corrections {
  width: 25em !important;
}

pre.editor-colors {
  background-color: #282c34;
  color: #abb2bf;
}
pre.editor-colors .line.cursor-line {
  background-color: rgba(153, 187, 255, 0.04);
}
pre.editor-colors .invisible {
  color: #abb2bf;
}
pre.editor-colors .cursor {
  border-left: 2px solid #528bff;
}
pre.editor-colors .selection .region {
  background-color: #3e4451;
}
pre.editor-colors .bracket-matcher .region {
  border-bottom: 1px solid #528bff;
  box-sizing: border-box;
}
pre.editor-colors .invisible-character {
  color: rgba(171, 178, 191, 0.15);
}
pre.editor-colors .indent-guide {
  color: rgba(171, 178, 191, 0.15);
}
pre.editor-colors .wrap-guide {
  background-color: rgba(171, 178, 191, 0.15);
}
pre.editor-colors .find-result .region.region.region,
pre.editor-colors .current-result .region.region.region {
  border-radius: 2px;
  background-color: rgba(82, 139, 255, 0.24);
  transition: border-color 0.4s;
}
pre.editor-colors .find-result .region.region.region {
  border: 2px solid transparent;
}
pre.editor-colors .current-result .region.region.region {
  border: 2px solid #528bff;
  transition-duration: .1s;
}
pre.editor-colors .gutter .line-number {
  color: #636d83;
  -webkit-font-smoothing: antialiased;
}
pre.editor-colors .gutter .line-number.cursor-line {
  color: #abb2bf;
  background-color: #2c313a;
}
pre.editor-colors .gutter .line-number.cursor-line-no-selection {
  background-color: transparent;
}
pre.editor-colors .gutter .line-number .icon-right {
  color: #abb2bf;
}
pre.editor-colors .gutter:not(.git-diff-icon) .line-number.git-line-removed.git-line-removed::before {
  bottom: -3px;
}
pre.editor-colors .gutter:not(.git-diff-icon) .line-number.git-line-removed::after {
  content: "";
  position: absolute;
  left: 0px;
  bottom: 0px;
  width: 25px;
  border-bottom: 1px dotted rgba(224, 82, 82, 0.5);
  pointer-events: none;
}
pre.editor-colors .gutter .line-number.folded,
pre.editor-colors .gutter .line-number:after,
pre.editor-colors .fold-marker:after {
  color: #abb2bf;
}
.syntax--comment {
  color: #5c6370;
  font-style: italic;
}
.syntax--comment .syntax--markup.syntax--link {
  color: #5c6370;
}
.syntax--entity.syntax--name.syntax--type {
  color: #e5c07b;
}
.syntax--entity.syntax--other.syntax--inherited-class {
  color: #98c379;
}
.syntax--keyword {
  color: #c678dd;
}
.syntax--keyword.syntax--control {
  color: #c678dd;
}
.syntax--keyword.syntax--operator {
  color: #abb2bf;
}
.syntax--keyword.syntax--other.syntax--special-method {
  color: #61afef;
}
.syntax--keyword.syntax--other.syntax--unit {
  color: #d19a66;
}
.syntax--storage {
  color: #c678dd;
}
.syntax--storage.syntax--type.syntax--annotation,
.syntax--storage.syntax--type.syntax--primitive {
  color: #c678dd;
}
.syntax--storage.syntax--modifier.syntax--package,
.syntax--storage.syntax--modifier.syntax--import {
  color: #abb2bf;
}
.syntax--constant {
  color: #d19a66;
}
.syntax--constant.syntax--variable {
  color: #d19a66;
}
.syntax--constant.syntax--character.syntax--escape {
  color: #56b6c2;
}
.syntax--constant.syntax--numeric {
  color: #d19a66;
}
.syntax--constant.syntax--other.syntax--color {
  color: #56b6c2;
}
.syntax--constant.syntax--other.syntax--symbol {
  color: #56b6c2;
}
.syntax--variable {
  color: #e06c75;
}
.syntax--variable.syntax--interpolation {
  color: #be5046;
}
.syntax--variable.syntax--parameter {
  color: #abb2bf;
}
.syntax--string {
  color: #98c379;
}
.syntax--string.syntax--regexp {
  color: #56b6c2;
}
.syntax--string.syntax--regexp .syntax--source.syntax--ruby.syntax--embedded {
  color: #e5c07b;
}
.syntax--string.syntax--other.syntax--link {
  color: #e06c75;
}
.syntax--punctuation.syntax--definition.syntax--comment {
  color: #5c6370;
}
.syntax--punctuation.syntax--definition.syntax--method-parameters,
.syntax--punctuation.syntax--definition.syntax--function-parameters,
.syntax--punctuation.syntax--definition.syntax--parameters,
.syntax--punctuation.syntax--definition.syntax--separator,
.syntax--punctuation.syntax--definition.syntax--seperator,
.syntax--punctuation.syntax--definition.syntax--array {
  color: #abb2bf;
}
.syntax--punctuation.syntax--definition.syntax--heading,
.syntax--punctuation.syntax--definition.syntax--identity {
  color: #61afef;
}
.syntax--punctuation.syntax--definition.syntax--bold {
  color: #e5c07b;
  font-weight: bold;
}
.syntax--punctuation.syntax--definition.syntax--italic {
  color: #c678dd;
  font-style: italic;
}
.syntax--punctuation.syntax--section.syntax--embedded {
  color: #be5046;
}
.syntax--punctuation.syntax--section.syntax--method,
.syntax--punctuation.syntax--section.syntax--class,
.syntax--punctuation.syntax--section.syntax--inner-class {
  color: #abb2bf;
}
.syntax--support.syntax--class {
  color: #e5c07b;
}
.syntax--support.syntax--type {
  color: #56b6c2;
}
.syntax--support.syntax--function {
  color: #56b6c2;
}
.syntax--support.syntax--function.syntax--any-method {
  color: #61afef;
}
.syntax--entity.syntax--name.syntax--function {
  color: #61afef;
}
.syntax--entity.syntax--name.syntax--class,
.syntax--entity.syntax--name.syntax--type.syntax--class {
  color: #e5c07b;
}
.syntax--entity.syntax--name.syntax--section {
  color: #61afef;
}
.syntax--entity.syntax--name.syntax--tag {
  color: #e06c75;
}
.syntax--entity.syntax--other.syntax--attribute-name {
  color: #d19a66;
}
.syntax--entity.syntax--other.syntax--attribute-name.syntax--id {
  color: #61afef;
}
.syntax--meta.syntax--class {
  color: #e5c07b;
}
.syntax--meta.syntax--class.syntax--body {
  color: #abb2bf;
}
.syntax--meta.syntax--method-call,
.syntax--meta.syntax--method {
  color: #abb2bf;
}
.syntax--meta.syntax--definition.syntax--variable {
  color: #e06c75;
}
.syntax--meta.syntax--link {
  color: #d19a66;
}
.syntax--meta.syntax--require {
  color: #61afef;
}
.syntax--meta.syntax--selector {
  color: #c678dd;
}
.syntax--meta.syntax--separator {
  background-color: #373b41;
  color: #abb2bf;
}
.syntax--meta.syntax--tag {
  color: #abb2bf;
}
.syntax--underline {
  text-decoration: underline;
}
.syntax--none {
  color: #abb2bf;
}
.syntax--invalid.syntax--deprecated {
  color: #523d14 !important;
  background-color: #e0c285 !important;
}
.syntax--invalid.syntax--illegal {
  color: white !important;
  background-color: #e05252 !important;
}
.syntax--markup.syntax--bold {
  color: #d19a66;
  font-weight: bold;
}
.syntax--markup.syntax--changed {
  color: #c678dd;
}
.syntax--markup.syntax--deleted {
  color: #e06c75;
}
.syntax--markup.syntax--italic {
  color: #c678dd;
  font-style: italic;
}
.syntax--markup.syntax--heading {
  color: #e06c75;
}
.syntax--markup.syntax--heading .syntax--punctuation.syntax--definition.syntax--heading {
  color: #61afef;
}
.syntax--markup.syntax--link {
  color: #56b6c2;
}
.syntax--markup.syntax--inserted {
  color: #98c379;
}
.syntax--markup.syntax--quote {
  color: #d19a66;
}
.syntax--markup.syntax--raw {
  color: #98c379;
}
.syntax--source.syntax--c .syntax--keyword.syntax--operator {
  color: #c678dd;
}
.syntax--source.syntax--cpp .syntax--keyword.syntax--operator {
  color: #c678dd;
}
.syntax--source.syntax--cs .syntax--keyword.syntax--operator {
  color: #c678dd;
}
.syntax--source.syntax--css .syntax--property-name,
.syntax--source.syntax--css .syntax--property-value {
  color: #828997;
}
.syntax--source.syntax--css .syntax--property-name.syntax--support,
.syntax--source.syntax--css .syntax--property-value.syntax--support {
  color: #abb2bf;
}
.syntax--source.syntax--gfm .syntax--markup {
  -webkit-font-smoothing: auto;
}
.syntax--source.syntax--gfm .syntax--link .syntax--entity {
  color: #61afef;
}
.syntax--source.syntax--go .syntax--storage.syntax--type.syntax--string {
  color: #c678dd;
}
.syntax--source.syntax--ini .syntax--keyword.syntax--other.syntax--definition.syntax--ini {
  color: #e06c75;
}
.syntax--source.syntax--java .syntax--storage.syntax--modifier.syntax--import {
  color: #e5c07b;
}
.syntax--source.syntax--java .syntax--storage.syntax--type {
  color: #e5c07b;
}
.syntax--source.syntax--java .syntax--keyword.syntax--operator.syntax--instanceof {
  color: #c678dd;
}
.syntax--source.syntax--java-properties .syntax--meta.syntax--key-pair {
  color: #e06c75;
}
.syntax--source.syntax--java-properties .syntax--meta.syntax--key-pair > .syntax--punctuation {
  color: #abb2bf;
}
.syntax--source.syntax--js .syntax--keyword.syntax--operator {
  color: #56b6c2;
}
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--delete,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--in,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--of,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--instanceof,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--new,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--typeof,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--void {
  color: #c678dd;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--string.syntax--quoted.syntax--json {
  color: #e06c75;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation.syntax--string {
  color: #e06c75;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation {
  color: #98c379;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--constant.syntax--language.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--constant.syntax--language.syntax--json {
  color: #56b6c2;
}
.syntax--source.syntax--ruby .syntax--constant.syntax--other.syntax--symbol > .syntax--punctuation {
  color: inherit;
}
.syntax--source.syntax--python .syntax--keyword.syntax--operator.syntax--logical.syntax--python {
  color: #c678dd;
}
.syntax--source.syntax--python .syntax--variable.syntax--parameter {
  color: #d19a66;
}
</style>
  </head>
  <body class='markdown-preview' data-use-github-style><h1 id="h-ng-d-n-c-i-t-openstack-newton-b-ng-packstack-tr-n-centos-7">Hướng dẫn cài đặt Openstack Newton bằng packstack trên CentOS 7</h1>
<h2 id="1-c-c-b-c-chu-n-b-tr-c-khi-c-i-t">1. Các bước chuẩn bị trước khi cài đặt</h2>
<h3 id="1-1-gi-i-thi-u">1.1 Giới thiệu</h3>
<ul>
<li>Packstack là một công cụ cài đặt OpenStack nhanh chóng.</li>
<li>Packstack được phát triển bởi redhat</li>
<li>Chỉ hỗ trợ các distro: RHEL, Centos</li>
<li>Tự động hóa các bước cài đặt và lựa chọn thành phần cài đặt.</li>
<li>Nhanh chóng dựng được môi trường OpenStack để sử dụng làm PoC nội bộ, demo khách hàng, test tính năng.</li>
<li>Nhược điểm 1 : Đóng kín các bước cài đối với người mới.</li>
<li>Nhược điểm 2: Khó bug các lỗi khi cài vì đã được đóng gói cùng với các tool cài đặt tự động (puppet)<h3 id="1-2-m-i-tr-ng-th-c-hi-n">1.2 Môi trường thực hiện</h3>
</li>
<li>Distro: CentOS 7.x</li>
<li>OpenStack Newton</li>
<li>NIC1 - ens3 : Là dải mạng mà các máy ảo sẽ giao tiếp với bên ngoài. Dải mạng này sử dụng chế độ bridge hoặc NAT của VMware Workstation</li>
<li>NIC2 - ens4: là dải mạng sử dụng cho các traffic MGNT + API + DATA VM. Dải mạng này sử dụng chế độ hostonly trong VMware Workstation<h3 id="1-3-m-h-nh">1.3 Mô hình</h3>
</li>
</ul>
<p><img src="http://i.imgur.com/dOIEhQF.png"></p>
<h3 id="1-4-ip-planning">1.4 IP Planning</h3>
<p><img src="http://i.imgur.com/Ddbj4mS.png"></p>
<h2 id="2-c-c-b-c-c-i-t">2. Các bước cài đặt</h2>
<h3 id="2-1-c-c-b-c-chu-n-b-tr-n-tr-n-controller">2.1. Các bước chuẩn bị trên trên Controller</h3>
<ul>
<li>Thiết lập hostname
hostnamectl set-hostname controller</li>
<li>Thiết lập IP</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>echo</span></span><span>&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>Setup&nbsp;IP&nbsp;&nbsp;ens3</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.addresses&nbsp;192.168.100.99/24</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.gateway&nbsp;192.168.100.1</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.dns&nbsp;8.8.8.8</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.method&nbsp;manual</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;con&nbsp;mod&nbsp;ens3&nbsp;connection.autoconnect&nbsp;yes</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>echo</span></span><span>&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>Setup&nbsp;IP&nbsp;&nbsp;ens4</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens4&nbsp;ipv4.addresses&nbsp;10.10.10.99/24</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens4&nbsp;ipv4.method&nbsp;manual</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;con&nbsp;mod&nbsp;ens4&nbsp;connection.autoconnect&nbsp;yes</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;disable&nbsp;firewalld</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;stop&nbsp;firewalld</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;disable&nbsp;NetworkManager</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;stop&nbsp;NetworkManager</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;</span><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>enable</span></span><span>&nbsp;network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;start&nbsp;network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sed&nbsp;-i&nbsp;</span><span class="syntax--string syntax--quoted syntax--single syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&#39;</span></span><span>s/SELINUX=enforcing/SELINUX=disabled/g</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&#39;</span></span></span><span>&nbsp;/etc/sysconfig/selinux</span></span></div></pre>
<ul>
<li>Khai báo repos cho OpenStack newton</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;yum&nbsp;install&nbsp;-y&nbsp;centos-release-openstack-newton</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>yum&nbsp;update&nbsp;-y</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;yum&nbsp;install&nbsp;-y&nbsp;wget&nbsp;crudini&nbsp;fping</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>yum&nbsp;install&nbsp;-y&nbsp;openstack-packstack</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>init&nbsp;6</span></span></div></pre>
<h3 id="2-2-c-c-b-c-chu-n-b-tr-n-tr-n-compute1">2.2. Các bước chuẩn bị trên trên Compute1</h3>
<ul>
<li><p>Thiết lập hostname</p>
<p><code>hostnamectl set-hostname compute1</code></p>
</li>
<li><p>Thiết lập IP</p>
</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>echo</span></span><span>&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>Setup&nbsp;IP&nbsp;&nbsp;ens3</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.addresses&nbsp;192.168.100.100/24</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.gateway&nbsp;192.168.100.1</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.dns&nbsp;8.8.8.8</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens3&nbsp;ipv4.method&nbsp;manual</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;con&nbsp;mod&nbsp;ens3&nbsp;connection.autoconnect&nbsp;yes</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>echo</span></span><span>&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>Setup&nbsp;IP&nbsp;&nbsp;ens4</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens4&nbsp;ipv4.addresses&nbsp;10.10.10.100/24</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;c&nbsp;modify&nbsp;ens4&nbsp;ipv4.method&nbsp;manual</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>nmcli&nbsp;con&nbsp;mod&nbsp;ens4&nbsp;connection.autoconnect&nbsp;yes</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;disable&nbsp;firewalld</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;stop&nbsp;firewalld</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;disable&nbsp;NetworkManager</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;stop&nbsp;NetworkManager</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;</span><span class="syntax--support syntax--function syntax--builtin syntax--shell"><span>enable</span></span><span>&nbsp;network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;systemctl&nbsp;start&nbsp;network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sed&nbsp;-i&nbsp;</span><span class="syntax--string syntax--quoted syntax--single syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&#39;</span></span><span>s/SELINUX=enforcing/SELINUX=disabled/g</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&#39;</span></span></span><span>&nbsp;/etc/sysconfig/selinux</span></span></div></pre>
<ul>
<li>Khai báo repos cho OpenStack newton</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;yum&nbsp;install&nbsp;-y&nbsp;centos-release-openstack-newton</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>yum&nbsp;update&nbsp;-y</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>sudo&nbsp;yum&nbsp;install&nbsp;-y&nbsp;wget&nbsp;crudini&nbsp;fping</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>yum&nbsp;install&nbsp;-y&nbsp;openstack-packstack</span></span></div></pre>
<h3 id="2-3-c-c-b-c-chu-n-b-tr-n-tr-n-compute2">2.3. Các bước chuẩn bị trên trên Compute2</h3>
<p>Làm tương tự như trên compute1</p>
<h3 id="2-4-b-t-u-c-i-t-packstack-tr-n-tr-n-controller">2.4. Bắt đầu cài đặt packstack trên trên Controller</h3>
<ul>
<li>Login vào máy chủ Controler và thực hiện các bước dưới bằng quyền root.</li>
<li>Thực hiện lệnh fping từ máy controller để kiểm tra các IP trên các máy đã thiết lập đúng hay chưa?</li>
</ul>
<p><code>fping 10.10.10.100 10.10.10.101</code></p>
<ul>
<li><p>Trong hướng dẫn này sẽ thực hiện cài đặt đồng thời 2 usecase về network của OpenStack, đó là Provider network và Self service network. Có nghĩa là máy ảo có thể gắn vào dải provider hoặc selfservice</p>
</li>
<li><p>SSH vào máy chủ Controller và thực hiện bằng quyền root</p>
</li>
<li><p>Sử dụng lệnh dưới để cài OpenStack.</p>
</li>
<li><p>Khi cài, màn hình sẽ yêu cầu nhập mật khẩu của các máy COM1 và COM2, sau đó packstack sẽ tự động cài trên các máy này mà ko cần thao tác.</p>
</li>
</ul>
<p>Sau khi hoàn tất. Truy cập vào web theo địa chỉ <a href="http://192.168.100.99/dashboard">http://192.168.100.99/dashboard</a>, tài khoản là admin, mật khẩu là Welcome123</p>
<h2 id="3-s-d-ng-openstack-sau-khi-c-i-t-xong-">3. Sử dụng OpenStack sau khi cài đặt xong.</h2>
<ul>
<li>Thực hiện lệnh dưới để khai báo biến môi trường mỗi khi đăng nhập phiên mới vào máy chủ.</li>
</ul>
<p><code>source /root/keystonerc_admin</code></p>
<ul>
<li>Kiểm tra trạng thái của các service NOVA bằng lệnh openstack compute service list, nếu state là up thì có thể tiếp tục các bước dưới.</li>
</ul>
<p><code>openstack compute service list</code></p>
<ul>
<li>Kiểm tra trạng thái của dịch vụ neutron bằng lệnh neutron agent-list, nếu có biểu tượng :) thì có thể tiếp tục bước dưới.</li>
</ul>
<p><code>neutron agent-list</code></p>
<h3 id="3-1-upload-image">3.1. Upload image</h3>
<ul>
<li>Thực thi biến môi trường</li>
</ul>
<p><code>source ~/keystonerc_admin</code></p>
<ul>
<li>upload image</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>curl&nbsp;http://download.cirros-cloud.net/0.3.4/cirros-0.3.4-x86_64-disk.img&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;glance&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>image-create&nbsp;--name=</span><span class="syntax--string syntax--quoted syntax--single syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&#39;</span></span><span>cirros</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&#39;</span></span></span><span>&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--visibility=public&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--container-format=bare&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--disk-format=qcow2</span></span></div></pre>
<h3 id="3-2-t-o-network-router">3.2. Tạo network, router</h3>
<ul>
<li>Tạo network public</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;net-create&nbsp;external_network&nbsp;--provider:network_type&nbsp;flat&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--provider:physical_network&nbsp;extnet&nbsp;&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--router:external&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--shared</span></span></div></pre>
<ul>
<li>Tạo subnet trong network public</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;subnet-create&nbsp;--name&nbsp;public_subnet&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--enable_dhcp=True&nbsp;--dns-nameserver&nbsp;8.8.8.8\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--allocation-pool=start=192.168.100.80,end=192.168.100.90\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--gateway=172.16.69.1&nbsp;external_network&nbsp;192.168.100.0/24</span></span></div></pre>
<ul>
<li>Tạo network private</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;net-create&nbsp;private_network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;subnet-create&nbsp;--name&nbsp;private_subnet&nbsp;private_network&nbsp;10.10.10.0/24&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--dns-nameserver&nbsp;8.8.8.8</span></span></div></pre>
<p><strong>Nếu gặp lỗi: Multiple network matches found for name &#39;private_network&#39;, use an ID to be more specific.</strong> thì ta thay <code>private_network</code> bằng ID. VD</p>
<p>Khi <code>neutron net-create private_network</code> sẽ hiển thị như sau:</p>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>Created&nbsp;a&nbsp;new&nbsp;network:</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+---------------------------+--------------------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Field&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Value&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+---------------------------+--------------------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;admin_state_up&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;availability_zone_hints&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;availability_zones&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;created_at&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;2017-07-17T06:40:09Z&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;description&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;id&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;e5366a8e-8a7b-4c12-be34-81092821e938&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;ipv4_address_scope&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;ipv6_address_scope&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;mtu&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;1450&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;private_network&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;project_id&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;8483de8077a34d3b8edff7da84ec7963&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;provider:network_type&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;vxlan&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;provider:physical_network&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;provider:segmentation_id&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;58&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;revision_number&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;router:external&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;False&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;shared&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;False&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;status&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;ACTIVE&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;subnets&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;tags&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;tenant_id&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;8483de8077a34d3b8edff7da84ec7963&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;updated_at&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;2017-07-17T06:40:09Z&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+---------------------------+--------------------------------------+</span></span></div></pre>
<p>Copy ID trong bảng trên thay vào private_network</p>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;subnet-create&nbsp;--name&nbsp;private_subnet&nbsp;</span><span class="syntax--keyword syntax--operator syntax--glob syntax--shell"><span>*</span></span><span>e5366a8e-8a7b-4c12-be34-81092821e938</span><span class="syntax--keyword syntax--operator syntax--glob syntax--shell"><span>*</span></span><span>&nbsp;10.10.10.0/24&nbsp;\</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>--dns-nameserver&nbsp;8.8.8.8</span></span></div></pre>
<ul>
<li>Tạo router tên là Vrouter và add các network vừa tạo ở trên vào router. Thực hiện lần lược từng câu lệnh</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;router-create&nbsp;Vrouter</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;router-gateway-set&nbsp;Vrouter</span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>ID</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span>&nbsp;external_network</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;router-interface-add&nbsp;Vrouter</span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>ID</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span>&nbsp;private_subnet</span></span></div></pre>
<p>Tương tự nếu gặp lỗi như trên ta cũng thay Vrouter ở dòng thứ 2 và 3 trong đoạn lệnh trên bằng mã ID </p>
<ul>
<li>Kiểm tra IP của router vừa được gán interface</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>neutron&nbsp;router-port-list&nbsp;12ecfceb-b926-40b0-9ebb-0aa7efde8371</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+------+-------------------+---------------------------------------------------------------------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;id&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;name&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;mac_address&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;fixed_ips&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+------+-------------------+---------------------------------------------------------------------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;0c058942-d544-4777-8fe3-69da28abd347&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;fa:16:3e:db:86:3c&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;{</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>subnet_id</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>:&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>d2ea77a8-1840-4b85-b940-0824eab873c2</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>,&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>ip_address</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>:&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>10.10.10.1</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;adea7ad3-a74d-48ef-8551-65b0c72323aa&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;fa:16:3e:ab:d6:df&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;{</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>subnet_id</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>:&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>c95bf9c4-fa38-402b-87bd-0d526721ee36</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>,&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>ip_address</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>:&nbsp;</span><span class="syntax--string syntax--quoted syntax--double syntax--shell"><span class="syntax--punctuation syntax--definition syntax--string syntax--begin syntax--shell"><span>&quot;</span></span><span>192.168.100.89</span><span class="syntax--punctuation syntax--definition syntax--string syntax--end syntax--shell"><span>&quot;</span></span></span><span>}&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+------+-------------------+---------------------------------------------------------------------------------------+</span></span></div></pre>
<p>12ecfceb-b926-40b0-9ebb-0aa7efde8371 là id của Vrouter</p>
<ul>
<li>Ping tới ip của dải provider để kiểm tra xem đã gán được interface hay chưa</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--meta syntax--scope syntax--logical-expression syntax--shell"><span class="syntax--punctuation syntax--definition syntax--logical-expression syntax--shell"><span>[</span></span><span>root@controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--tilde syntax--shell"><span>~</span></span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>keystone_admin</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span class="syntax--punctuation syntax--definition syntax--logical-expression syntax--shell"><span>]</span></span></span><span class="syntax--comment syntax--line syntax--number-sign syntax--shell"><span class="syntax--punctuation syntax--definition syntax--comment syntax--shell"><span>#</span></span><span>&nbsp;ping&nbsp;192.168.100.89</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>PING&nbsp;192.168.100.89&nbsp;</span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>192.168.100.89</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span>&nbsp;56</span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>84</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span>&nbsp;bytes&nbsp;of&nbsp;data.</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>64&nbsp;bytes&nbsp;from&nbsp;192.168.100.89:&nbsp;icmp_seq=1&nbsp;ttl=64&nbsp;time=0.597&nbsp;ms</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>64&nbsp;bytes&nbsp;from&nbsp;192.168.100.89:&nbsp;icmp_seq=2&nbsp;ttl=64&nbsp;time=0.044&nbsp;ms</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>64&nbsp;bytes&nbsp;from&nbsp;192.168.100.89:&nbsp;icmp_seq=3&nbsp;ttl=64&nbsp;time=0.039&nbsp;ms</span></span></div></pre>
<ul>
<li>Mở các rule cần thiết cho máy ảo (trong thực tế nên mở các rule cần thiết, tránh mở tất cả các port như hướng dẫn này)</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>openstack&nbsp;security&nbsp;group&nbsp;rule&nbsp;create&nbsp;--proto&nbsp;icmp&nbsp;default</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>openstack&nbsp;security&nbsp;group&nbsp;rule&nbsp;create&nbsp;--proto&nbsp;tcp&nbsp;--dst-port&nbsp;1:65535&nbsp;default</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>openstack&nbsp;security&nbsp;group&nbsp;rule&nbsp;create&nbsp;--proto&nbsp;udp&nbsp;--dst-port&nbsp;1:65535&nbsp;default</span></span></div></pre>
<p>Trước khi truy cập vào dashboad ta chỉnh sửa 1 vài lỗi </p>
<ul>
<li><p>Lỗi không nhận metadata
Sửa file /etc/neutron/dhcp_agent.ini trên Controller node</p>
<p><code>vi /etc/neutron/dhcp_agent.ini</code></p>
<p>Bỏ comment vào sửa như sau:</p>
<p><code>enable_isolated_metadata = True</code></p>
<p>Khởi động lại các service của neutron trên Controller node.</p>
</li>
</ul>
<pre class="editor-colors lang-sh"><div class="line"><span class="syntax--source syntax--shell"><span>&nbsp;&nbsp;</span><span class="syntax--meta syntax--scope syntax--logical-expression syntax--shell"><span class="syntax--punctuation syntax--definition syntax--logical-expression syntax--shell"><span>[</span></span><span>root@controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--tilde syntax--shell"><span>~</span></span><span class="syntax--meta syntax--scope syntax--subshell syntax--shell"><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>(</span></span><span>keystone_admin</span><span class="syntax--punctuation syntax--definition syntax--subshell syntax--shell"><span>)</span></span></span><span class="syntax--punctuation syntax--definition syntax--logical-expression syntax--shell"><span>]</span></span></span><span class="syntax--comment syntax--line syntax--number-sign syntax--shell"><span class="syntax--punctuation syntax--definition syntax--comment syntax--shell"><span>#</span></span><span>&nbsp;neutron&nbsp;agent-list</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+--------------------+------------+-------------------+-------+----------------+---------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;id&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;agent_type&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;host&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;availability_zone&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;alive&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;admin_state_up&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;binary&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+--------------------+------------+-------------------+-------+----------------+---------------------------+</span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;61e342d2-91c6-434c-976a-3fb2c7cd5e7a&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Metering&nbsp;agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-metering-agent&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;6cb93409-5969-4393-bd7a-cb36bcac2124&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Open&nbsp;vSwitch&nbsp;agent&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;compute1&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-openvswitch-agent&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;9ad40459-1a35-409f-9f84-09ef0a8db76c&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;DHCP&nbsp;agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;nova&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-dhcp-agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;bb28bd00-9124-4cb4-94a1-209bd429bdf0&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Metadata&nbsp;agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-metadata-agent&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;dda53f34-909c-425c-916d-08b75cb76545&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;L3&nbsp;agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;nova&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-l3-agent&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;e6a3cfb2-8f3a-425d-8172-62cdf457b4eb&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;Open&nbsp;vSwitch&nbsp;agent&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;controller&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;:-)&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;True&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span><span>&nbsp;neutron-openvswitch-agent&nbsp;</span><span class="syntax--keyword syntax--operator syntax--pipe syntax--shell"><span>|</span></span></span></div><div class="line"><span class="syntax--source syntax--shell"><span>+--------------------------------------+--------------------+------------+-------------------+-------+----------------+---------------------------+</span></span></div></pre>
<ul>
<li><p>Lỗi không kết nối được tới console, gặp phải khi chạy máy ảo với nhiều node compute</p>
<p>Thay hostname trong dòng dưới ở file /etc/nova/nova.conf bằng IP của chính máy compute đó.</p>
<p><code>vncserver_proxyclient_address=192.168.100.100</code></p>
<p>Restart lại dịch vụ openstack-nova-compute</p>
</li>
</ul>
<h2 id="4-s-d-ng-dashboad">4. Sử dụng dashboad</h2>
<h3 id="4-1-t-o-m-y-o">4.1. Tạo máy ảo</h3>
<p>Đăng nhập vào dashboad và thưc hiện theo bước sau:</p>
<ul>
<li>Click vào tab <code>Instances</code> và chọn <code>Launch Instance</code></li>
<li>Trong tab Details, nhập tên máy ảo </li>
</ul>
<p><img src="http://i.imgur.com/cERpFfO.png"></p>
<ul>
<li>Trong tab Source chọn images cho máy ảo</li>
</ul>
<p><img src="http://i.imgur.com/iofgHvD.png"></p>
<ul>
<li>Trong tab Flavor chọn kích thước của máy ảo </li>
</ul>
<p><img src="http://i.imgur.com/8GnnmGw.png"></p>
<ul>
<li>Trong tab Network chọn dải mạng mà máy ảo sẽ gắn vào. Trong ví dụ này chọn dải external, nếu chọn dải private thì cần thực hiện bước floating IP. </li>
</ul>
<p><img src="http://i.imgur.com/2dsADhq.png"></p>
<p>Chờ máy máy khởi tạo và thưc hiện ping, ssh để kiểm tra với IP được cấp trên dashboad</p></body>
</html>
