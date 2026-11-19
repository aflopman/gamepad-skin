/*
 GameSir Tarantula 8K PC - Gamepad Viewer custom skin
 Base image: official GameSir product image (Shopify CDN)
 Designed for GamepadViewer compact mode (?p=1&css=...)

 Hosted on GitHub, load it with (jsDelivr or raw.githubusercontent.com):
   https://cdn.jsdelivr.net/gh/<user>/<repo>@main/gamesir-tarantula-8k-custom.css
   https://raw.githubusercontent.com/<user>/<repo>/main/gamesir-tarantula-8k-custom.css
*/

/* Base layer: the whole GameSir photo, top-aligned at 1000px wide.
   The press indicators below are positioned against this exact layout. */
.controller.custom {
  position: relative;
  width: 1000px;
  height: 1000px;
  background-image: url("https://cdn.shopify.com/s/files/1/2241/8433/files/gamesir-tarantula-8k-pc-wired-esports-controller-for-pc-9496467.png?quality=75&v=1785969188&width=2560");
  background-repeat: no-repeat;
  background-size: 1000px auto;
  background-position: center top;
}

/* Hide the stock Xbox graphics; the GameSir photo is the base layer. */
.controller.custom .triggers,
.controller.custom .bumpers,
.controller.custom .quadrant,
.controller.custom .arrows,
.controller.custom .abxy,
.controller.custom .sticks,
.controller.custom .dpad {
  pointer-events: none;
}

/* Trigger press indicators */
.custom .trigger {
  position: absolute;
  width: 110px;
  height: 70px;
  opacity: 0;
  border-radius: 22px;
  background: rgba(255,255,255,.28);
  box-shadow: 0 0 22px rgba(255,255,255,.9), inset 0 0 12px rgba(255,255,255,.7);
}
.custom .trigger.left { left: 255px; top: 190px; }
.custom .trigger.right { right: 255px; top: 190px; }
.custom .trigger.pressed { opacity: 1; }

/* Bumper press indicators */
.custom .bumper {
  position: absolute;
  width: 100px;
  height: 30px;
  opacity: 0;
  border-radius: 15px;
  background: rgba(255,255,255,.25);
  box-shadow: 0 0 18px rgba(255,255,255,.9);
}
.custom .bumper.left { left: 285px; top: 230px; }
.custom .bumper.right { right: 285px; top: 230px; }
.custom .bumper.pressed { opacity: 1; }

/* Face-button press indicators */
.custom .abxy {
  position: absolute;
  left: 635px;
  top: 265px;
  width: 170px;
  height: 170px;
}
.custom .button {
  position: absolute;
  width: 52px;
  height: 52px;
  border-radius: 50%;
  background: rgba(255,255,255,.20);
  box-shadow: 0 0 18px rgba(255,255,255,.85);
  opacity: 0;
}
.custom .button.pressed { opacity: 1; }

.custom .a { left: 60px; top: 105px; }
.custom .b { left: 112px; top: 52px; }
.custom .x { left: 8px; top: 52px; }
.custom .y { left: 60px; top: 0; }

/* D-pad press indicators */
.custom .dpad {
  position: absolute;
  left: 205px;
  top: 270px;
  width: 150px;
  height: 150px;
}
.custom .face {
  position: absolute;
  background: rgba(255,255,255,.28);
  box-shadow: 0 0 16px rgba(255,255,255,.8);
  opacity: 0;
}
.custom .face.up,
.custom .face.down { width: 42px; height: 55px; left: 54px; }
.custom .face.left,
.custom .face.right { width: 55px; height: 42px; top: 54px; }
.custom .face.up { top: 0; }
.custom .face.down { top: 95px; }
.custom .face.left { left: 0; }
.custom .face.right { right: 0; }
.custom .face.pressed { opacity: 1; }

/* Analog-stick indicators: the actual Gamepad Viewer JS still moves these. */
.custom .sticks {
  position: absolute;
  left: 315px;
  top: 395px;
  width: 370px;
  height: 180px;
}
.custom .stick {
  position: absolute;
  width: 82px;
  height: 82px;
  border-radius: 50%;
  background: rgba(0,0,0,.18);
  border: 3px solid rgba(255,255,255,.45);
  box-shadow: inset 0 0 12px rgba(0,0,0,.6), 0 0 12px rgba(255,255,255,.25);
}
.custom .stick.left { left: 0; top: 0; }
.custom .stick.right { right: 0; bottom: 0; }
.custom .stick.pressed {
  border-color: rgba(255,255,255,.95);
  box-shadow: inset 0 0 12px rgba(255,255,255,.35), 0 0 22px rgba(255,255,255,.95);
}

/* Start / Menu / View indicators */
.custom .back,
.custom .start {
  position: absolute;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  opacity: 0;
  background: rgba(255,255,255,.35);
  box-shadow: 0 0 18px rgba(255,255,255,.9);
}
.custom .back.pressed,
.custom .start.pressed { opacity: 1; }

/* Disconnected state: keep the photo, hide the indicator elements. */
.custom.disconnected div { display: none; }
