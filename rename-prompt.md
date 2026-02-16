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
      "title": "Grykonx | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Grykonx | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7cd3c01f553780097ebe1c4668033bfe.css",
    "context": {
      "path": "css/7cd3c01f553780097ebe1c4668033bfe.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
    }
  },
  {
    "path": "css/923d7a12989d8629b2276bcb808c92b9.css",
    "context": {
      "path": "css/923d7a12989d8629b2276bcb808c92b9.css"
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
    "path": "imgs/054c324072303951de9af8047450cc48.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08543939e1fda746e64e6eb0382b86a7.webp",
    "context": {
      "refs": [
        {
          "alt": "Every small business owner knows the importance of their business data. Could your business weather ",
          "title": ""
        },
        {
          "alt": "Business Continuity Planning",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b8e01f0162c38f832ff21a1a6c29637.webp",
    "context": {
      "refs": [
        {
          "alt": "Healthcare",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12782eaacf2111a412a8e91fd5e2377c.webp",
    "context": {
      "refs": [
        {
          "alt": "Retail",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1715fe89fa9eed1a5479f39204af4958.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1726a1f7664d3aa85f04e361cde330a6.webp",
    "context": {
      "refs": [
        {
          "alt": "Manufacturing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e3fce41b90182717132e509705cfe93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/333d7210b723b5ef44377e0b028466d7.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/341af88e9ddbf75d00bee791473b2373.webp",
    "context": {
      "refs": [
        {
          "alt": "Annual Maintenance Contracts",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/383375292f107e4816467f09f2cb900c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3feb6f8277bfac2b5160368c1af7b0e5.webp",
    "context": {
      "refs": [
        {
          "alt": "Virtualization provides unmatched flexibility, performance, and utilization by allowing you to move ",
          "title": ""
        },
        {
          "alt": "Web Development",
          "title": ""
        },
        {
          "alt": "Virtualization",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/460719cd29299d0f60326e209e892398.webp",
    "context": {
      "refs": [
        {
          "alt": "In GrykonX we have Consultants who are ideally positioned to assess your business needs and to integ",
          "title": ""
        },
        {
          "alt": "Network Design and Support",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/468cacab769e10cc1d39e918174bc3e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/50b20147412bc012120dbd0444bc11cc.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5343e24027a917b0a535777889fc1615.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5819b3c4ead2e7468a28052b45622cec.webp",
    "context": {
      "refs": [
        {
          "alt": "Consulting",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b1e061a0b9cf22d11327fbb7fe30708.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bcaeb74b55be9956e8414e68352489b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6077d8c1513737f4c28692bbb581731e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/630fde07f625df0dec6bf76eeaeda505.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64152ae380786cfaec69c991c0b7f781.webp",
    "context": {
      "refs": [
        {
          "alt": "Industry Served Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64222b37e4fab4b7c4381d6a57709997.webp",
    "context": {
      "refs": [
        {
          "alt": "We understand technology and the impact it can have on your business; that\u2019s why our support offerin",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6505f4272a32d8fae1ec53d6501496d3.webp",
    "context": {
      "refs": [
        {
          "alt": "Cloud services and computing solutions allow you and your employees to share, edit, and publish docu",
          "title": ""
        },
        {
          "alt": "Cloud Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6631d88ace96315f61a08030d7ce7fdc.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7255950448eb14f99943f6df0d8701d5.webp",
    "context": {
      "refs": [
        {
          "alt": "Infrastructure Review",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/760950c6f0ba15508e5aa67a59a1d66a.webp",
    "context": {
      "refs": [
        {
          "alt": "Accounting",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7791dedb31c49b45b7d453021caa6dca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/789f2ddd5fff4514db0305caf524b1dc.webp",
    "context": {
      "refs": [
        {
          "alt": "Whether you need IT planning services , network and server support, network consulting and integrati",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7eade04dca9bff6cc5c4a76de60bb00e.webp",
    "context": {
      "refs": [
        {
          "alt": "We employ the latest technology to provide a complete security offering with 24\u00d77 monitoring availab",
          "title": ""
        },
        {
          "alt": "Security Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81963f32ada5ace969937d03bb10e170.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82a75e46457ed6f94cddde663996bd29.webp",
    "context": {
      "refs": [
        {
          "alt": "Facility Management & Corporate Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d67c5690da540688ea35ac0d789d68a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8dbe905ecb20f08c7fb3e61419e6e46b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/914c370ed7e7639ef66aa5479b3616f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9347941403bc594b7873215b1496c3e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/984bc3f98311333261453a1f95e4ecb9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c6deafdbd83a0b195bf2f40b432078f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af8be1e5f295fec2038504ef1aff6391.webp",
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
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6ef17a18805d26507fc40a3326b9cd9.webp",
    "context": {
      "refs": [
        {
          "alt": "Storage Area Networks",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7d9c63e51a4428916a6e165c3d363a7.webp",
    "context": {
      "refs": [
        {
          "alt": "Project Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b97c86933296fb45ba4d3974a3614dc1.webp",
    "context": {
      "refs": [
        {
          "alt": "Strategic Advice",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1723a73000f1d6547e62a617f78886e.webp",
    "context": {
      "refs": [
        {
          "alt": "m",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c563cee4c20f9b64bac951601fce60e4.webp",
    "context": {
      "refs": [
        {
          "alt": "Coming Soon",
          "title": ""
        },
        {
          "alt": "Oriented Companies",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca348e520350cb5dac5f530c1f8305fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d21da4020fb33e926c8d455e64304e18.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3dbb2e6ab334b1d4bab820f9c71551e.webp",
    "context": {
      "refs": [
        {
          "alt": "Hardware & Software Procurement",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9536338dd0cd2a402dd9e50e952c613.webp",
    "context": {
      "refs": [
        {
          "alt": "Rental Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9e467d028e3acc9eb8826339085e42b.webp",
    "context": {
      "refs": [
        {
          "alt": "Technology Consulting Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e3825d0919f82a3c4c9756deb21825ad.webp",
    "context": {
      "refs": [
        {
          "alt": "Legal",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec7939f6355400d8d1d6252b41aa7b4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f01645d304fb349b2112f243b80928a5.webp",
    "context": {
      "refs": [
        {
          "alt": "Structured Cabling",
          "title": ""
        },
        {
          "alt": "Structured Cabling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0668ce950e7bcffe324ecb6de3c13ea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4af1b9bf9df2a8cb60ea972bf9aa929.webp",
    "context": {
      "refs": [
        {
          "alt": "From design to day-to-day support, we manage your data center infrastructure and maintain a highly q",
          "title": ""
        },
        {
          "alt": "Data Center Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f7404c88dafc11ef2b069a5b85bc75a3.webp",
    "context": {
      "refs": [
        {
          "alt": "Grykonx provides a full range of business-grade telephone hardware and services. Our solutions are f",
          "title": ""
        },
        {
          "alt": "Business Phone Systems",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb0758d0968dd67f3c4a43dcc153ee5a.webp",
    "context": {
      "refs": [
        {
          "alt": "Construction",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ffbede826401aed3ee573e89c5d52ae0.webp",
    "context": {
      "refs": [
        {
          "alt": "Firewall, Antivirus and Antispam",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ffcfb7a4f153bac54847c27167426f98.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Grykonx | Beyond Technology",
      "first_heading": "GrykonX"
    }
  },
  {
    "path": "industries.html",
    "context": {
      "title": "Grykonx | Industries",
      "first_heading": "INDUSTRIES"
    }
  },
  {
    "path": "js/024c2427a07d4754d082b32ff6f47796.js",
    "context": {
      "path": "js/024c2427a07d4754d082b32ff6f47796.js"
    }
  },
  {
    "path": "js/027151cf1be95681de1b467942001858.js",
    "context": {
      "path": "js/027151cf1be95681de1b467942001858.js"
    }
  },
  {
    "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js",
    "context": {
      "path": "js/20ebc5f4fff22d9c0b0df7a66b7d8c8a.js"
    }
  },
  {
    "path": "js/2d36e9fa24b491802cf18f39a308190c.js",
    "context": {
      "path": "js/2d36e9fa24b491802cf18f39a308190c.js"
    }
  },
  {
    "path": "js/2d62c5e761d3e1992478716162667ce5.js",
    "context": {
      "path": "js/2d62c5e761d3e1992478716162667ce5.js"
    }
  },
  {
    "path": "js/328ee378638a24926abf5dec969f9194.js",
    "context": {
      "path": "js/328ee378638a24926abf5dec969f9194.js"
    }
  },
  {
    "path": "js/3e734a79111d3ae5022fadd97f4b4570.js",
    "context": {
      "path": "js/3e734a79111d3ae5022fadd97f4b4570.js"
    }
  },
  {
    "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js",
    "context": {
      "path": "js/3f434054cfbcb9efddefc25bf53a0b2b.js"
    }
  },
  {
    "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js",
    "context": {
      "path": "js/425f5d74616f0950ab7f6aa8a2ba3011.js"
    }
  },
  {
    "path": "js/4a184d88eb9269b7dbce11b716f40379.js",
    "context": {
      "path": "js/4a184d88eb9269b7dbce11b716f40379.js"
    }
  },
  {
    "path": "js/56848c032b05f79a1c67ea6d7b451252.js",
    "context": {
      "path": "js/56848c032b05f79a1c67ea6d7b451252.js"
    }
  },
  {
    "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js",
    "context": {
      "path": "js/5cd7f03eb032ff5d1a79d9daad244677.js"
    }
  },
  {
    "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js",
    "context": {
      "path": "js/61ce9c6e209c2c6687f8b2e0bb0fa78f.js"
    }
  },
  {
    "path": "js/6432203ce192bdda9fff6890193487b5.js",
    "context": {
      "path": "js/6432203ce192bdda9fff6890193487b5.js"
    }
  },
  {
    "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js",
    "context": {
      "path": "js/7b9a1dfa2ba7ebd6966eb4b5a2b8cccf.js"
    }
  },
  {
    "path": "js/7d7d8ec406a653220337bde42ddcd998.js",
    "context": {
      "path": "js/7d7d8ec406a653220337bde42ddcd998.js"
    }
  },
  {
    "path": "js/969912c5e1cdd73b7812defd4dbd0119.js",
    "context": {
      "path": "js/969912c5e1cdd73b7812defd4dbd0119.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js",
    "context": {
      "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js"
    }
  },
  {
    "path": "js/aeea5981f09059b3304ead8b513e8042.js",
    "context": {
      "path": "js/aeea5981f09059b3304ead8b513e8042.js"
    }
  },
  {
    "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js",
    "context": {
      "path": "js/afe09ede095ecb21a7d57d52891fbfe8.js"
    }
  },
  {
    "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js",
    "context": {
      "path": "js/bd271374cbdbf6b93a861a0d1da4d44b.js"
    }
  },
  {
    "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js",
    "context": {
      "path": "js/c0a73d949973f41fdb7cb5098a95c51d.js"
    }
  },
  {
    "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js",
    "context": {
      "path": "js/d1ec9a5167f878e894e5532ac741f0dd.js"
    }
  },
  {
    "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js",
    "context": {
      "path": "js/d2a524fa5eb75b486a06e4ccd15439a7.js"
    }
  },
  {
    "path": "js/dd2afe6604cc9bb429a5b0cb3c0860f8.js",
    "context": {
      "path": "js/dd2afe6604cc9bb429a5b0cb3c0860f8.js"
    }
  },
  {
    "path": "js/e83b51d598b2a45483252c3be82d77b0.js",
    "context": {
      "path": "js/e83b51d598b2a45483252c3be82d77b0.js"
    }
  },
  {
    "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js",
    "context": {
      "path": "js/f17632f1cc1088a1c285f0d8e9cedde0.js"
    }
  },
  {
    "path": "js/f5b6708cffe7c1147c483017fbec7d58.js",
    "context": {
      "path": "js/f5b6708cffe7c1147c483017fbec7d58.js"
    }
  },
  {
    "path": "managed-services.html",
    "context": {
      "title": "Grykonx | IT Services",
      "first_heading": "MANAGED IT SERVICES"
    }
  },
  {
    "path": "partners.html",
    "context": {
      "title": "Grykonx | Alliances & Partnership",
      "first_heading": "ALLIANCES & PARTNERSHIP"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "Grykonx | INFRASTRUCTURE SERVICES",
      "first_heading": "INFRASTRUCTURE SERVICES"
    }
  },
  {
    "path": "software-web-developement.html",
    "context": {
      "title": "Grykonx | Software And Web Developement",
      "first_heading": "SOFTWARE AND WEB DEVELOPEMENT"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.