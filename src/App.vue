<template>
  <div id="app">

  </div>
</template>

<script>
import hljs from 'highlight.js'

export default {
  name: 'app',
  mounted () {
    hljs.initHighlightingOnLoad()
  }
}

</script>

<style lang="stylus">
// font faces
$body-font = 'Source Sans Pro', 'Helvetica Neue', Arial, sans-serif
$logo-font = 'Dosis', 'Source Sans Pro', 'Helvetica Neue', Arial, sans-serif
$code-font = 'Roboto Mono', Monaco, courier, monospace

// font sizes
$body-font-size = 15px
$code-font-size = .8em

// colors
$dark   = #2c3e50
$medium = #34495e
$light  = #7f8c8d
$green  = #42b983
$border = #dddddd
$codebg = #f8f8f8
$red = #ff6666

$radius = 2px
$content-padding-top = 30px
$header-inner-height = 41px
$heading-padding-vertical = 10px
$header-height = $header-inner-height + $heading-padding-vertical * 2
$mobile-header-height = 40px
$heading-link-padding-top = $header-height + $content-padding-top
$mobile-heading-link-padding-top = $mobile-header-height + $content-padding-top
$h2-margin-top = 45px
$h3-margin-top = 52px

.highlight
    overflow-x auto
    position relative
    padding 0
    background-color $codebg
    padding .8em .8em .4em
    line-height 1.1em
    border-radius $radius
    table, tr, td
        width 100%
        border-collapse collapse
        padding 0
        margin 0
    .gutter
        width 1.5em
    .code
        $code-line-height = 1.5em
        pre
            padding 1.2em 1.4em
            line-height $code-line-height
            margin 0
        .line
            min-height $code-line-height
    &.html, &.js, &.bash, &.css
        .code:after
            position absolute
            top 0
            right 0
            color #ccc
            text-align right
            font-size .75em
            padding 5px 10px 0
            line-height 15px
            height 15px
            font-weight 600
    &.html .code:after
        content 'HTML'
    &.js .code:after
        content 'JS'
    &.bash .code:after
        content 'Shell'
    &.css .code:after
        content 'CSS'


.gutter pre
  color #999

pre
  color: #525252
  .function .keyword,
  .constant
    color: #0092db
  .keyword,
  .attribute
    color: #e96900
  .number,
  .literal
    color: #AE81FF
  .tag,
  .tag .title,
  .change,
  .winutils,
  .flow,
  .lisp .title,
  .clojure .built_in,
  .nginx .title,
  .tex .special
    color: #2973b7
  .class .title
    color: white
  .symbol,
  .symbol .string,
  .value,
  .regexp
    color: $green
  .title
    color: #A6E22E
  .tag .value,
  .string,
  .subst,
  .haskell .type,
  .preprocessor,
  .ruby .class .parent,
  .built_in,
  .sql .aggregate,
  .django .template_tag,
  .django .variable,
  .smalltalk .class,
  .javadoc,
  .django .filter .argument,
  .smalltalk .localvars,
  .smalltalk .array,
  .attr_selector,
  .pseudo,
  .addition,
  .stream,
  .envvar,
  .apache .tag,
  .apache .cbracket,
  .tex .command,
  .prompt
    color: $green
  .comment,
  .java .annotation,
  .python .decorator,
  .template_comment,
  .pi,
  .doctype,
  .deletion,
  .shebang,
  .apache .sqbracket,
  .tex .formula
    color: #b3b3b3
  .coffeescript .javascript,
  .javascript .xml,
  .tex .formula,
  .xml .javascript,
  .xml .vbscript,
  .xml .css,
  .xml .cdata
    opacity: 0.5

body
  font-family 'Roboto Mono', Monaco, courier, monospace
  -webkit-font-smoothing initial
  -moz-osx-font-smoothing initial

/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
