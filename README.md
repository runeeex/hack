<html>
  <head>
    <title>Hacked by RUN3X</title>
  </head>
  <body>
    <style>
      body {
        font-family: monospace;
        background: url("https://www.walldevil.com/wallpapers/w02/810234-anonymous-black-background-dark-v-for-vendetta.jpg")
          #000 no-repeat;
        background-size: 100%;
      }
      #slogan {
        text-align: center;
        font-size: 65px;
        color: #fff;
        position: relative;
        left: 50%;
        transform: translate(-50%, -50%);
      }
      #slogan span {
        color: #cb0000;
      }
      #slogan span.selected {
        background: #09f;
        color: #fff;
      }
    </style>

    <table width="100%" height="100%">
      <td align="center">
        <div id="slogan" data-text="HI, RUN3X WAS HERE!"></div>
      </td>
    </table>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>

    <script>
      (function ($) {
        $.fn.typer = function (options) {
          var defaults = $.extend(
            {
              search: "",
              replace: [],
              speed: 50,
              delay: 2000,
            },
            options
          );

          var bintext = function (length) {
            var text = "";
            for (var $i = 0; $i <= length; $i++) {
              text = text + Math.floor(Math.random() * 2);
            }
            return text;
          };

          this.each(function () {
            var $this = $(this);
            var $text = $this.data("text");
            var position = 0;

            var indexOf = $text.indexOf(defaults.search);
            var normal = $text.substr(0, indexOf);
            var changer = $text.substr(indexOf, $text.length);

            defaults.replace.push(changer);

            var interval = setInterval(function () {
              var $bintext = "";

              if (position == indexOf) {
                $bintext = bintext(changer.length - 1);

                $this.html($text.substr(0, normal.length));
                $this.append("<span>" + $bintext + "</span>");
              } else if (position > indexOf) {
                $bintext = bintext($text.length - 1);

                $this
                  .delay(defaults.speed)
                  .find("span")
                  .html(
                    changer.substring(0, position - indexOf) +
                      $bintext.substring(position, $bintext.length)
                  );
              } else if (position < indexOf) {
                $bintext = bintext($text.length - 1);

                $this
                  .delay(defaults.speed)
                  .html(
                    normal.substring(0, position) +
                      $bintext.substring(position, $bintext.length)
                  );
              }

              if (position < $text.length) {
                position++;
              } else {
                clearInterval(interval);

                var index = 0;
                setInterval(function () {
                  var position = 0;
                  var newText = defaults.replace[index];

                  var changeInterval = setInterval(function () {
                    var $bintext = "";
                    for (var $i = 0; $i <= newText.length - 1; $i++) {
                      $bintext = $bintext + Math.floor(Math.random() * 2);
                    }

                    $this
                      .delay(defaults.speed)
                      .find("span")
                      .html(
                        newText.substring(0, position) +
                          $bintext.substring(position, $bintext.length)
                      );

                    if (position < $text.length) {
                      position++;
                    } else {
                      clearInterval(changeInterval);
                    }
                  }, defaults.speed);

                  if (index < defaults.replace.length - 1) {
                    index++;
                  } else {
                    index = 0;
                  }
                }, defaults.delay);
              }
            }, defaults.speed);
          });
        };
      })(jQuery);

      $(function () {
        $("#slogan").typer({
          search: "RUN3X WAS HERE!",
          replace: [
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
            "RUN3X WAS HERE!",
          ],
        });
      });
    </script>

    <script>
      document.addEventListener("contextmenu", function (e) {
        e.preventDefault();
        alert("Sorry, Inspect element is disabled. - UniteError");
      });

      document.onkeydown = function (e) {
        if (event.keyCode == 123) {
          return false;
        }

        if (e.ctrlKey && e.shiftKey && e.keyCode == "I".charCodeAt(0)) {
          return false;
        }

        if (e.ctrlKey && e.shiftKey && e.keyCode == "C".charCodeAt(0)) {
          return false;
        }

        if (e.ctrlKey && e.shiftKey && e.keyCode == "J".charCodeAt(0)) {
          return false;
        }

        if (e.ctrlKey && e.keyCode == "U".charCodeAt(0)) {
          return false;
        }
      };
    </script>

    <audio
      src="https://nathanprinsley-files.prinsh.com/data-1/mp3/best-hacker-music.mp3"
      loop="1"
      autoplay="1"
    ></audio>
  </body>
</html>
