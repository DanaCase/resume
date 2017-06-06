<template>
      <div class="row">
        
        <svg id="hexagon" preserveAspectRatio="xMidYMin" :viewBox=points.viewBox :height=points.height :width=points.width>
          <text :font-size=fontSizeFirst x="50%" :y=firstY alignment-baseline="middle" text-anchor="middle" font-family='Unna' font-style="italic" :fill=svgColor>DANA</text>
          <text :font-size=fontSizeLast x="50%" :y=lastY alignment-baseline="middle" text-anchor="middle" font-family='Unna' font-style="italic" :fill=svgColor>CASE</text>

          <polyline :stroke=svgColor fill="none" :stroke-width=accentStrokeWidth :points=points.topPathString></polyline>
          <polyline :stroke=svgColor fill="none" :stroke-width=accentStrokeWidth :points=points.bottomPathString></polyline>
          <polygon class="hex"  fill="none" :stroke=svgColor :stroke-width=strokeWidth :points=points.pathString alignment-baseline=middle></polygon>
        
        </svg>
      </div>
</template>

<script>
  export default {
    name: 'hexagon',
    data: () => {
      return {
        points: new Points(300, 300 * Math.sqrt(3) / 2),
        strokeWidth: 4.5,
        accentStrokeWidth: 4,
        svgColor: '#555'
      }
    },
    computed: {
      firstY: function () {
        return this.points.height / 2 - (this.points.height / 15)
      },
      lastY: function () {
        return this.firstY + this.fontSizeFirst
      },
      fontSizeFirst: function () {
        return this.points.height * 0.18
      },
      fontSizeLast: function () {
        return this.fontSizeFirst * 0.75
      }
    },
    mounted: function () {
      var width = window.getComputedStyle(this.$el.parentElement, null).getPropertyValue('width').slice(0, -2)
      this.points = new Points(width, width)
    }

  }
  function Points (height, width) {
    function pathsToString (paths) {
      var strings = paths.map((points) => points.join(','))
      return strings.join(' ')
    }

    var [ pathHeight, pathWidth ] = [ height * 0.89, width * 0.78 ]
    var [ offsetHeight, offsetWidth ] = [ (height - pathHeight) / 2, (width - pathWidth) / 2 ]
    var path = [
      [ pathWidth / 2 + offsetWidth, offsetHeight ],
      [ pathWidth + offsetWidth, pathHeight * 0.25 + offsetHeight ],
      [ pathWidth + offsetWidth, pathHeight * 0.75 + offsetHeight ],
      [ pathWidth / 2 + offsetWidth, pathHeight + offsetHeight ],
      [ offsetWidth, pathHeight * 0.75 + offsetHeight ],
      [ offsetWidth, pathHeight * 0.25 + offsetHeight ]
    ]
    this.pathString = pathsToString(path)

    var bottomPaths = [
      [ path[2][0], path[2][1] - 10 ],
      [ path[3][0], path[3][1] - 10 ],
      [ path[4][0], path[4][1] - 10 ]
    ]
    this.bottomPathString = pathsToString(bottomPaths)

    var topPaths = [
      [ path[5][0], path[5][1] + 10 ],
      [ path[0][0], path[0][1] + 10 ],
      [ path[1][0], path[1][1] + 10 ]
    ]
    this.topPathString = pathsToString(topPaths)

    this.viewBox = [ -2.5, -2.5, height, width ].join(',')

    this.height = height
    this.width = width
  }
</script>

