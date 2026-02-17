You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Aadgad Remedies | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Aadgad Remedies | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/058e717ec5f282b0007e7d8b83584c8b.webp",
    "context": {
      "refs": [
        {
          "alt": "OOKAI DSR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/108f467b0a955ce8bc85109aa6aef40a.webp",
    "context": {
      "refs": [
        {
          "alt": "Ursomail-300",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10aadea0ae2be0357b28727a6525c86e.webp",
    "context": {
      "refs": [
        {
          "alt": "CenturiCAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12725e549ac3bbff8f5fdd421b20a2b6.webp",
    "context": {
      "refs": [
        {
          "alt": "Boltagesic-Pas",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1da55e8065d0d080a4c5634a82d777cf.webp",
    "context": {
      "refs": [
        {
          "alt": "About Us - Aadgad Remedies",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fe5fdaf8a95c8de6602bf9465689c41.webp",
    "context": {
      "refs": [
        {
          "alt": "Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2995214ea22861865ed80fe171c22d61.webp",
    "context": {
      "refs": [
        {
          "alt": "OOKAI LS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ae80f78709ca4621aa1278e3cc2e1e5.webp",
    "context": {
      "refs": [
        {
          "alt": "OOKAI-4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3404e3d89b08c301429f50b1a619a7e2.webp",
    "context": {
      "refs": [
        {
          "alt": "Tibacef 200",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/368edac9a114684190ad7fd2c499fd94.webp",
    "context": {
      "refs": [
        {
          "alt": "Tibaclav",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e2268f1f41a5ca81626622f290446df.webp",
    "context": {
      "refs": [
        {
          "alt": "Lookast Forte",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ccd47caf3c5c3ac872a336f9a1f75ed.webp",
    "context": {
      "refs": [
        {
          "alt": "Nurturing Relationships",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d4dc9f8434bf666093cdfa587e7c34b.webp",
    "context": {
      "refs": [
        {
          "alt": "IM-6/30",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7247608ea6e2c9c0f9bc04a77f4ff214.webp",
    "context": {
      "refs": [
        {
          "alt": "Fifteen-Plus",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c8b96e89b48ba68227fc66433007df2.webp",
    "context": {
      "refs": [
        {
          "alt": "Boltagesic-120",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9dba8ccae76e24bf697b656e539873e4.webp",
    "context": {
      "refs": [
        {
          "alt": "MMVIT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e25ab08a5f6f8a5c9d11d115d908d04.webp",
    "context": {
      "refs": [
        {
          "alt": "Lookast-LC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2fd9de25a7bd77a8bfb953cced0ebe0.webp",
    "context": {
      "refs": [
        {
          "alt": "FIFTEEN-PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b754cf4247251ba44ce579aea35a47ec.webp",
    "context": {
      "refs": [
        {
          "alt": "Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9e4213f1de0aaaa3e41acdcf2c8b91e.webp",
    "context": {
      "refs": [
        {
          "alt": "Goutmatic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7127b9a24d120b64081f82a1895adb2.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7214f6607dd42cc70eabb648857efa3.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/eed12dfb5c520eabb8691e2dc93b4f98.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Distribution & Network",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe00031381cfdc4ea6db2483ba9b2128.webp",
    "context": {
      "refs": [
        {
          "alt": "Tibapod-200",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Aadgad Remedies | Home",
      "first_heading": "Aadgad Remedies"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "Aadgad Remedies | Products",
      "first_heading": "PRODUCTS"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.