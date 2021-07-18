<template>
  <div class="home">
    <div class="container mt-4">
      <div class="row">
        <div class="col">
          <YouTubeSearchResultList v-bind:youtubeSearchResults="youtubeQueryResults" />
        </div>
        <div class="col">
          <SearchBox v-on:search-query="fetchSearchQuery" />
          <WikipediaSearchResultList
            v-bind:wikipediaSearchResults="queryResults"
          />
        </div>
        <div class="col">
          <TMDBSearchResultList v-bind:tmdbSearchResults="tmdbQueryResults" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SearchBox from "@/components/commons/SearchBox";
import WikipediaSearchResultList from "@/components/wikipedia/WikipediaSearchResultList";
import TMDBSearchResultList from "@/components/tmdb/TMDBSearchResultList";
import YouTubeSearchResultList from '@/components/youtube/YouTubeSearchResultList';
import axios from "axios";

export default {
  name: "Home",
  components: {
    SearchBox,
    WikipediaSearchResultList,
    TMDBSearchResultList,
YouTubeSearchResultList
  },
  data() {
    return {
      queryResults: [],
      // wikiQueryResults: [],
      tmdbQueryResults: [],
      youtubeQueryResults: []
    };
  },
  methods: {
    fetchSearchQuery(query) {
      this.searchWiki(query);
      this.searchTMDB(query);
      this.searchYouTube(query);
    },
    searchYouTube(query) {
      query
      // axios
      //   .get(
      //     `https://www.googleapis.com/youtube/v3/search?part=snippet&maxResults=5&q=${query}&key=AIzaSyBLybr_kj97vCugo_TbiwGlQhXn9oM9vpQ`
      //   )
      //   .then((res) => {
      //     this.youtubeQueryResults = res.data.items;// grab on first top 5 search results
      //   })
      //   .catch((err) => console.log(err));

      this.youtubeQueryResults = 

[
    {
      "kind": "youtube#searchResult",
      "etag": "rfkJ3jRUwDgCUeXfXSVr2wTkCWw",
      "id": {
        "kind": "youtube#video",
        "videoId": "W37XjX0cKPg"
      },
      "snippet": {
        "publishedAt": "2021-07-17T12:00:25Z",
        "channelId": "UCrk_7ovk1tv9sEgFv6kwpog",
        "title": "China is kicking out foreigners?",
        "description": "Are foreigners welcomed in China? Why many expats who lived in China for years are now forced to leave? | Get MY BOOK 'I lived in Shanghai' on Amazon!",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/W37XjX0cKPg/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/W37XjX0cKPg/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/W37XjX0cKPg/hqdefault.jpg",
            "width": 480,
            "height": 360
          }
        },
        "channelTitle": "by Kaja 凯娅",
        "liveBroadcastContent": "none",
        "publishTime": "2021-07-17T12:00:25Z"
      }
    },
    {
      "kind": "youtube#searchResult",
      "etag": "xG_ow1MfN_3meVyDZI1dsamUofk",
      "id": {
        "kind": "youtube#video",
        "videoId": "onVqYtX2_7U"
      },
      "snippet": {
        "publishedAt": "2021-07-16T13:37:54Z",
        "channelId": "UCrp_UI8XtuYfpiqluWLD7Lw",
        "title": "China vows to retaliate if U.S. imposes more sanctions over Hong Kong",
        "description": "CNBC's Eunice Yoon reports on the reaction to the Biden administration warning U.S. companies about the situation in Hong Kong. For access to live and ...",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/onVqYtX2_7U/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/onVqYtX2_7U/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/onVqYtX2_7U/hqdefault.jpg",
            "width": 480,
            "height": 360
          }
        },
        "channelTitle": "CNBC Television",
        "liveBroadcastContent": "none",
        "publishTime": "2021-07-16T13:37:54Z"
      }
    },
    {
      "kind": "youtube#searchResult",
      "etag": "dkODOOsomeLPmW3Gg50i7P77NKA",
      "id": {
        "kind": "youtube#video",
        "videoId": "iSaElW4yMHI"
      },
      "snippet": {
        "publishedAt": "2021-07-17T19:14:55Z",
        "channelId": "UC5BMIWZe9isJXLZZWPWvBlg",
        "title": "Singapura, Amerika Serikat, dan China Beri Bantuan untuk Indonesia Tangani Pandemi Corona",
        "description": "KOMPAS.TV - Sejumlah negara telah mengirimkan bantuan untuk Indonesia dalam rangka penanganan pandemi corona. Yang pertama ada negara tetangga, ...",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/iSaElW4yMHI/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/iSaElW4yMHI/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/iSaElW4yMHI/hqdefault.jpg",
            "width": 480,
            "height": 360
          }
        },
        "channelTitle": "KOMPASTV",
        "liveBroadcastContent": "none",
        "publishTime": "2021-07-17T19:14:55Z"
      }
    },
    {
      "kind": "youtube#searchResult",
      "etag": "knTyNWuKdsXqXkVdxvgRrLd-LeM",
      "id": {
        "kind": "youtube#video",
        "videoId": "xGwrevM_n_g"
      },
      "snippet": {
        "publishedAt": "2021-07-16T02:43:15Z",
        "channelId": "UCpWvshQVx1d7BqCsPnVuNIw",
        "title": "WHO: China should provide raw data on pandemic&#39;s origins",
        "description": "WHO Director-General Tedros Adhanom Ghebreyesus on Thursday (July 15) said that investigations into the origins of the Covid-19 pandemic in China were ...",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/xGwrevM_n_g/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/xGwrevM_n_g/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/xGwrevM_n_g/hqdefault.jpg",
            "width": 480,
            "height": 360
          }
        },
        "channelTitle": "The Star",
        "liveBroadcastContent": "none",
        "publishTime": "2021-07-16T02:43:15Z"
      }
    },
    {
      "kind": "youtube#searchResult",
      "etag": "6Z0SMp_WH3B0l1iNvtoqlK-tx9Q",
      "id": {
        "kind": "youtube#video",
        "videoId": "ckNcPkxTJvU"
      },
      "snippet": {
        "publishedAt": "2021-07-15T13:30:05Z",
        "channelId": "UCx8Z14PpntdaxCt2hakbQLQ",
        "title": "India China trade में कैसे हुई बढ़ोतरी | Mastercard | Modi government | DA | Kharcha Pani Ep 120",
        "description": "Please download 5paisa app - https://www.5paisa.com/landing/zomato-ipo-offer?",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/ckNcPkxTJvU/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/ckNcPkxTJvU/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/ckNcPkxTJvU/hqdefault.jpg",
            "width": 480,
            "height": 360
          }
        },
        "channelTitle": "The Lallantop",
        "liveBroadcastContent": "none",
        "publishTime": "2021-07-15T13:30:05Z"
      }
    }
  ]
    },
    searchWiki(query) {
      axios
        .get(
          `https://en.wikipedia.org/w/api.php?action=query&format=json&origin=*&list=search&srsearch=${query}`
        )
        .then((res) => {
          this.queryResults = res.data.query.search;
          this.queryResults = this.queryResults.slice(0, 5); // grab on first top 5 search results
        })
        .catch((err) => console.log(err));
    },
    searchTMDB(query) {
      axios
        .get(
          `https://api.themoviedb.org/3/search/multi?api_key=1a7eb2f78daf0c6f300f6b339f4f5030&language=en-US&query=${query}&page=1&include_adult=false`
        )
        .then((res) => {
          this.tmdbQueryResults = res.data.results;
          this.tmdbQueryResults = this.tmdbQueryResults.slice(0, 5);
        })
        .catch((err) => console.log(err));
    },
  },
  // show the latest movie releases and trending YouTube Videos at initial load.
  created() {
    axios
      .get(
        `https://api.themoviedb.org/3/trending/all/day?api_key=1a7eb2f78daf0c6f300f6b339f4f5030`
      )
      .then((res) => {
        this.tmdbQueryResults = res.data.results;
        this.tmdbQueryResults = this.tmdbQueryResults.slice(0, 5);
      })
      .catch((err) => console.log(err));


      // axios
      //   .get(
      //   `https://www.googleapis.com/youtube/v3/videos?chart=mostPopular&key=AIzaSyBLybr_kj97vCugo_TbiwGlQhXn9oM9vpQ&part=snippet&maxResults=5`)
      //   .then((res) => {
      //     console.log(res)
      //     this.youtubeQueryResults = res.data.items;// grab on first top 5 search results
      //   })
      //   .catch((err) => console.log(err));
      this.youtubeQueryResults = 
  [
    {
      "kind": "youtube#video",
      "etag": "WvYp306CFnYEFtnNmWWrOANVD8c",
      "id": "DFMEBquxeO8",
      "snippet": {
        "publishedAt": "2021-07-16T04:00:08Z",
        "channelId": "UCpd3rXPsHKu1nRnUyxEm1xQ",
        "title": "Normani - Wild Side (Official Video) ft. Cardi B",
        "description": "Normani feat. Cardi B – “Wild Side” Out Now!\nListen Now: https://normaniwildside.com \n\nhttps://smarturl.it/xWildSide\nhttps://smarturl.it/xWildSide/officialstore\nhttps://smarturl.it/xWildSide/applemusic\nhttps://smarturl.it/xWildSide/spotify\nhttps://smarturl.it/xWildSide/youtubemusic\nhttps://smarturl.it/xWildSide/tidal\nhttps://smarturl.it/xWildSide/pandora\nhttps://smarturl.it/xWildSide/soundcloud\nhttps://smarturl.it/xWildSide/itunes\nhttps://smarturl.it/xWildSide/deezer\n\nFollow Normani:\nhttps://www.twitter.com/Normani  \nhttps://www.facebook.com/normanikordei \nhttps://www.instagram.com/normani/\n\nFollow Cardi B:\nhttp://www.twitter.com/IAmCardiB \nhttp://www.facebook.com/IAmCardiB \nhttps://www.instagram.com/iamcardib/ \n\nDirected by: Tanu Muino\nProduced by: Jack Winter\nExecutive Produced by: Frank Borin, Ivanna Borin\nLabel Producers - Camille Yorrick & Chris Clavadetscher\n\nCreative Director: Maxime Quoilin\nManagement: Brandon Silverstein and Jay Cao for S10 Entertainment\n\nProduction Co: UnderWonder Content\nCinematographer: Nikita Kuzmenko\nProduction Designer: Spencer Graves\nChoreographer: Sean Bankhead\n1st AD: Braden Anderson\nLocation Manager: Max Simon\nEditor: Vinnie Hobbs @ VHpost\nColor: Joseph Bicknell @ CO3\nVFX: Max Colt @ FRENDER\n  \nStylist: Kollin Carter\nNormani MU: Priscilla Ono\nNormani Hair: Yusef Williams\nNormani Nails: Sojin Oh\nDancer Hair: Ashanti Lation\nDancer Hair: Davontae Washington\nDancer MU: Hayley Kassel\nDancer MU: Jordana Aguon\nDancer MU: Kasha Lassien\n\n#Normani #CardiB #WildSide #OfficialVideo",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/DFMEBquxeO8/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/DFMEBquxeO8/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/DFMEBquxeO8/hqdefault.jpg",
            "width": 480,
            "height": 360
          },
          "standard": {
            "url": "https://i.ytimg.com/vi/DFMEBquxeO8/sddefault.jpg",
            "width": 640,
            "height": 480
          },
          "maxres": {
            "url": "https://i.ytimg.com/vi/DFMEBquxeO8/maxresdefault.jpg",
            "width": 1280,
            "height": 720
          }
        },
        "channelTitle": "NormaniVEVO",
        "tags": [
          "Normani wild side",
          "normai cardi b",
          "cardi b wild side",
          "wild side music video",
          "normani new music",
          "normani motivation",
          "cardi b up",
          "normani cardi b leak",
          "normani live",
          "normani Aaliyah",
          "Aaliyah one in a million",
          "normani dancing",
          "cardi b feature",
          "cardi b kulture",
          "cardi b wap",
          "normani ft cardi b",
          "normani wild side snippet",
          "normani wap",
          "cardi b new song",
          "cardi b normani",
          "cardi b megan thee stallion",
          "cardi b ne wsong 2021",
          "normani new song 2021",
          "music"
        ],
        "categoryId": "10",
        "liveBroadcastContent": "none",
        "localized": {
          "title": "Normani - Wild Side (Official Video) ft. Cardi B",
          "description": "Normani feat. Cardi B – “Wild Side” Out Now!\nListen Now: https://normaniwildside.com \n\nhttps://smarturl.it/xWildSide\nhttps://smarturl.it/xWildSide/officialstore\nhttps://smarturl.it/xWildSide/applemusic\nhttps://smarturl.it/xWildSide/spotify\nhttps://smarturl.it/xWildSide/youtubemusic\nhttps://smarturl.it/xWildSide/tidal\nhttps://smarturl.it/xWildSide/pandora\nhttps://smarturl.it/xWildSide/soundcloud\nhttps://smarturl.it/xWildSide/itunes\nhttps://smarturl.it/xWildSide/deezer\n\nFollow Normani:\nhttps://www.twitter.com/Normani  \nhttps://www.facebook.com/normanikordei \nhttps://www.instagram.com/normani/\n\nFollow Cardi B:\nhttp://www.twitter.com/IAmCardiB \nhttp://www.facebook.com/IAmCardiB \nhttps://www.instagram.com/iamcardib/ \n\nDirected by: Tanu Muino\nProduced by: Jack Winter\nExecutive Produced by: Frank Borin, Ivanna Borin\nLabel Producers - Camille Yorrick & Chris Clavadetscher\n\nCreative Director: Maxime Quoilin\nManagement: Brandon Silverstein and Jay Cao for S10 Entertainment\n\nProduction Co: UnderWonder Content\nCinematographer: Nikita Kuzmenko\nProduction Designer: Spencer Graves\nChoreographer: Sean Bankhead\n1st AD: Braden Anderson\nLocation Manager: Max Simon\nEditor: Vinnie Hobbs @ VHpost\nColor: Joseph Bicknell @ CO3\nVFX: Max Colt @ FRENDER\n  \nStylist: Kollin Carter\nNormani MU: Priscilla Ono\nNormani Hair: Yusef Williams\nNormani Nails: Sojin Oh\nDancer Hair: Ashanti Lation\nDancer Hair: Davontae Washington\nDancer MU: Hayley Kassel\nDancer MU: Jordana Aguon\nDancer MU: Kasha Lassien\n\n#Normani #CardiB #WildSide #OfficialVideo"
        }
      }
    },
    {
      "kind": "youtube#video",
      "etag": "i2W9P8bviX98Hj2bvYcIs7yEm50",
      "id": "oghoRsE1rDw",
      "snippet": {
        "publishedAt": "2021-07-17T15:00:20Z",
        "channelId": "UCpi8TJfiA4lKGkaXs__YdBA",
        "title": "The Try Guys Bake Macarons Without A Recipe",
        "description": "We've got two new bakers in the Try Kitchen today and we're all eager to see who will bake the sweetest little thing! It's episode two of the #WithoutARecipe summer season and it's macarON baby! Get your very own Try Guys Apron & Oven Mitts on https://tryguys.com/ today!\n\nAre you a business looking to work with The Try Guys? Reach out to us at 2ndtrybusiness@gmail.com for all business inquiries! \n\n🎧THE TRYPOD 🎧: watch our new podcast at https://youtube.com/trypod or listen at https://tryguys.com/podcast\n\n📘THE HIDDEN POWER OF F*CKING UP 📘: check out our new book at https://tryguys.com/book\n\nGet your official Try Guys color hoodies and phone cases at https://tryguys.com/collections/color-line 💙❤️💚💜\n\nSupport us! http://www.patreon.com/tryguys. Join our Patreon to get videos a day early, plus, live streams, chatrooms, BTS footage, exclusive merchandise, and more!\n\nSUBSCRIBE TO AND FOLLOW THE TRY GUYS \nhttp://www.youtube.com/c/tryguys\nhttp://www.facebook.com/tryguys  \nhttp://www.twitter.com/tryguys\nhttps://www.instagram.com/tryguys\n\nFOLLOW THE GUYS\nhttp://www.Instagram.com/keithhabs\nhttp://www.Instagram.com/nedfulmer\nhttp://www.Instagram.com/korndiddy\nhttp://www.instagram.com/eugeneleeyang\n \nhttp://www.twitter.com/keithhabs\nhttp://www.twitter.com/nedfulmer \nhttp://www.twitter.com/korndiddy\nhttp://www.twitter.com/eugeneleeyang \n\nTHE TRY GUYS\nThe #TryGuys is the flagship channel of 2ND TRY, LLC. Tune in twice a week for shows from Keith, Ned, Zach and Eugene, the creators and stars of The Try Guys.\n\nAPPEARANCES\nRosanna Pansino - TV Host, Baker & YouTuber\nCheck out all of her amazing cooking content online!\nWebsite: http://www.RosannaPansino.com\nYouTube: @RosannaPansino https://www.youtube.com/user/RosannaPansino\nInstagram: @rosannapansino http://instagram.com/rosannapansino\nTwitter: @rosannapansino  http://twitter.com/rosannapansino\n\nRome & Cam from Dormtainment - check them out on YouTube and social media!\n@Dormtainment \nRome Green: @iromealot\nCameron Miller: @camfromdt\n\nUyen Kirshenbaum\nMichelin Starred Pastry Chef\nFind her work on Instagram: @kirshbakingco\n\nEDITED BY\nYB Chang @xoybox\n\nVoice Over\nTed Evans \n\nIllustration\nColleen Tighe\n\nPost Sound Mix \nCable Adkins\n\nEPISODE CREW\n\nDirected by Rachel Ann Cole\nDawn Shim - Director of Photography\nBen Hecht - Camera Operator\nDaryl Gilmore - Camera Operator\nRichie Yau - Camera Operator\nZoe Lubeck - 1st Assistant Camera\nMaria Arango - 1st Assistant Camera\nShay Eberle-Gunst - 1st Assistant Camera\nStephen St. Peter - Gaffer\nLogan Wade - Gaffer\nSusannah Honey - Production Designer\nJesse Ross- Art Production Assistant\nNiki Ford - Food Stylist \nMihyun Mia Han - Art Production Assistant\nJared Irlbeck - Set Builder  \nAlessia Madau - Art Production Assistant \nKevin Bazell - Sound Mixer \nScott Neff - Boom Operator\nJesse Martinez - Production Assistant\nAnthony Godinez - Production Assistant\n\n\nMUSIC\nLicensed from AudioNetwork\n\nSFX\nLicensed from Audioblocks\n\nVIDEO\nLicensed from Videoblocks\n\nOfficial Try Guys Photos \nBy Mandee Johnson Photography | @mandeephoto\n\n2nd Try, LLC STAFF\nExecutive Producer - Keith Habersberger\nExecutive Producer - Ned Fulmer\nExecutive Producer - Zach Kornfeld\nExecutive Producer - Eugene Lee Yang\nProducer - Rachel Ann Cole\nProducer - Nick Rufca\nAssociate Producer - Alexandria Herring\nEditor - Devlin McCluskey\nEditor - YB Chang\nEditor - Elliot Dickerhoof\nAssistant Editor - Will Witwer\nPodcast Producer - Miles Bonsignore\nCamera Operator/Assistant Production Coordinator - Jonathan Kirk\nSound Operator Assistant Production Coordinator - Sam Johnson\nBrand Manager - Kaylin Burke\n\nSpecial Thanks To! \n\nThanks to all of our Gold Level Patrons! Athena, AJ S., Amy Fleming, Ana Camba, Cat Hicks, Elisa Proust, Emma Godfrey, Erica Rao, Jared Aarons, Kelsey Bock, Kourtney Wong, Loretta Wen, Matthew Tadros, Miha, Paulus, Sarah Waxman, Traci Lew, Wendy Tran, Lily",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/oghoRsE1rDw/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/oghoRsE1rDw/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/oghoRsE1rDw/hqdefault.jpg",
            "width": 480,
            "height": 360
          },
          "standard": {
            "url": "https://i.ytimg.com/vi/oghoRsE1rDw/sddefault.jpg",
            "width": 640,
            "height": 480
          },
          "maxres": {
            "url": "https://i.ytimg.com/vi/oghoRsE1rDw/maxresdefault.jpg",
            "width": 1280,
            "height": 720
          }
        },
        "channelTitle": "The Try Guys",
        "tags": [
          "try guys",
          "keith",
          "ned",
          "zach",
          "eugene",
          "habersberger",
          "fulmer",
          "kornfeld",
          "yang",
          "buzzfeedvideo",
          "buzzfeed",
          "ariel",
          "ned & ariel",
          "comedy",
          "education",
          "funny",
          "try",
          "learn",
          "fail",
          "experiment",
          "test",
          "tryceratops",
          "without a recipe",
          "cooking",
          "challenge",
          "cooking challenge",
          "how to cook",
          "baking muffins",
          "baking",
          "baking show",
          "food show",
          "easy muffin recipe",
          "how to make",
          "macarons",
          "french macarons",
          "how to make macarons",
          "perfect macarons",
          "macaron",
          "french macarons recipe",
          "best macarons",
          "homemade macarons",
          "macaron recipe",
          "macaroon"
        ],
        "categoryId": "23",
        "liveBroadcastContent": "none",
        "defaultLanguage": "en",
        "localized": {
          "title": "The Try Guys Bake Macarons Without A Recipe",
          "description": "We've got two new bakers in the Try Kitchen today and we're all eager to see who will bake the sweetest little thing! It's episode two of the #WithoutARecipe summer season and it's macarON baby! Get your very own Try Guys Apron & Oven Mitts on https://tryguys.com/ today!\n\nAre you a business looking to work with The Try Guys? Reach out to us at 2ndtrybusiness@gmail.com for all business inquiries! \n\n🎧THE TRYPOD 🎧: watch our new podcast at https://youtube.com/trypod or listen at https://tryguys.com/podcast\n\n📘THE HIDDEN POWER OF F*CKING UP 📘: check out our new book at https://tryguys.com/book\n\nGet your official Try Guys color hoodies and phone cases at https://tryguys.com/collections/color-line 💙❤️💚💜\n\nSupport us! http://www.patreon.com/tryguys. Join our Patreon to get videos a day early, plus, live streams, chatrooms, BTS footage, exclusive merchandise, and more!\n\nSUBSCRIBE TO AND FOLLOW THE TRY GUYS \nhttp://www.youtube.com/c/tryguys\nhttp://www.facebook.com/tryguys  \nhttp://www.twitter.com/tryguys\nhttps://www.instagram.com/tryguys\n\nFOLLOW THE GUYS\nhttp://www.Instagram.com/keithhabs\nhttp://www.Instagram.com/nedfulmer\nhttp://www.Instagram.com/korndiddy\nhttp://www.instagram.com/eugeneleeyang\n \nhttp://www.twitter.com/keithhabs\nhttp://www.twitter.com/nedfulmer \nhttp://www.twitter.com/korndiddy\nhttp://www.twitter.com/eugeneleeyang \n\nTHE TRY GUYS\nThe #TryGuys is the flagship channel of 2ND TRY, LLC. Tune in twice a week for shows from Keith, Ned, Zach and Eugene, the creators and stars of The Try Guys.\n\nAPPEARANCES\nRosanna Pansino - TV Host, Baker & YouTuber\nCheck out all of her amazing cooking content online!\nWebsite: http://www.RosannaPansino.com\nYouTube: @RosannaPansino https://www.youtube.com/user/RosannaPansino\nInstagram: @rosannapansino http://instagram.com/rosannapansino\nTwitter: @rosannapansino  http://twitter.com/rosannapansino\n\nRome & Cam from Dormtainment - check them out on YouTube and social media!\n@Dormtainment \nRome Green: @iromealot\nCameron Miller: @camfromdt\n\nUyen Kirshenbaum\nMichelin Starred Pastry Chef\nFind her work on Instagram: @kirshbakingco\n\nEDITED BY\nYB Chang @xoybox\n\nVoice Over\nTed Evans \n\nIllustration\nColleen Tighe\n\nPost Sound Mix \nCable Adkins\n\nEPISODE CREW\n\nDirected by Rachel Ann Cole\nDawn Shim - Director of Photography\nBen Hecht - Camera Operator\nDaryl Gilmore - Camera Operator\nRichie Yau - Camera Operator\nZoe Lubeck - 1st Assistant Camera\nMaria Arango - 1st Assistant Camera\nShay Eberle-Gunst - 1st Assistant Camera\nStephen St. Peter - Gaffer\nLogan Wade - Gaffer\nSusannah Honey - Production Designer\nJesse Ross- Art Production Assistant\nNiki Ford - Food Stylist \nMihyun Mia Han - Art Production Assistant\nJared Irlbeck - Set Builder  \nAlessia Madau - Art Production Assistant \nKevin Bazell - Sound Mixer \nScott Neff - Boom Operator\nJesse Martinez - Production Assistant\nAnthony Godinez - Production Assistant\n\n\nMUSIC\nLicensed from AudioNetwork\n\nSFX\nLicensed from Audioblocks\n\nVIDEO\nLicensed from Videoblocks\n\nOfficial Try Guys Photos \nBy Mandee Johnson Photography | @mandeephoto\n\n2nd Try, LLC STAFF\nExecutive Producer - Keith Habersberger\nExecutive Producer - Ned Fulmer\nExecutive Producer - Zach Kornfeld\nExecutive Producer - Eugene Lee Yang\nProducer - Rachel Ann Cole\nProducer - Nick Rufca\nAssociate Producer - Alexandria Herring\nEditor - Devlin McCluskey\nEditor - YB Chang\nEditor - Elliot Dickerhoof\nAssistant Editor - Will Witwer\nPodcast Producer - Miles Bonsignore\nCamera Operator/Assistant Production Coordinator - Jonathan Kirk\nSound Operator Assistant Production Coordinator - Sam Johnson\nBrand Manager - Kaylin Burke\n\nSpecial Thanks To! \n\nThanks to all of our Gold Level Patrons! Athena, AJ S., Amy Fleming, Ana Camba, Cat Hicks, Elisa Proust, Emma Godfrey, Erica Rao, Jared Aarons, Kelsey Bock, Kourtney Wong, Loretta Wen, Matthew Tadros, Miha, Paulus, Sarah Waxman, Traci Lew, Wendy Tran, Lily"
        },
        "defaultAudioLanguage": "en"
      }
    },
    {
      "kind": "youtube#video",
      "etag": "9nfvrfEo42Y9LKpzjgw2IriLaUU",
      "id": "hs0jo0n1OYM",
      "snippet": {
        "publishedAt": "2021-07-16T19:00:20Z",
        "channelId": "UCKQ-wNdh0kO5qnpPfXa2hjQ",
        "title": "Making American Food in a Place That is NOT America",
        "description": "BUY MY YOUTOOZ! https://youtooz.com/collections/ranboo\n\nI am in the UK now, so I decided to make the most American food possible to feel more at home. Subscribe for more amazing American meals.\n\nI am LIVE on\nhttps://www.twitch.tv/Ranboolive\u200b\u200b\nI say dumb things\nhttps://twitter.com/Ranboosaysstuff\u200b\u200b\nMERCH!:\nhttps://youtooz.com/collections/ranboo\nDISCORD:\nhttps://discord.com/invite/ranboo\u200b\u200b\nHave an awesome day!",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/hs0jo0n1OYM/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/hs0jo0n1OYM/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/hs0jo0n1OYM/hqdefault.jpg",
            "width": 480,
            "height": 360
          },
          "standard": {
            "url": "https://i.ytimg.com/vi/hs0jo0n1OYM/sddefault.jpg",
            "width": 640,
            "height": 480
          },
          "maxres": {
            "url": "https://i.ytimg.com/vi/hs0jo0n1OYM/maxresdefault.jpg",
            "width": 1280,
            "height": 720
          }
        },
        "channelTitle": "Ranboo",
        "tags": [
          "Ranboo",
          "Ranboo burger",
          "Tubbo",
          "Ranboo Tubbo",
          "Ranboolive",
          "Ranboo funny moments",
          "Comedy",
          "Commentary"
        ],
        "categoryId": "24",
        "liveBroadcastContent": "none",
        "localized": {
          "title": "Making American Food in a Place That is NOT America",
          "description": "BUY MY YOUTOOZ! https://youtooz.com/collections/ranboo\n\nI am in the UK now, so I decided to make the most American food possible to feel more at home. Subscribe for more amazing American meals.\n\nI am LIVE on\nhttps://www.twitch.tv/Ranboolive\u200b\u200b\nI say dumb things\nhttps://twitter.com/Ranboosaysstuff\u200b\u200b\nMERCH!:\nhttps://youtooz.com/collections/ranboo\nDISCORD:\nhttps://discord.com/invite/ranboo\u200b\u200b\nHave an awesome day!"
        },
        "defaultAudioLanguage": "en"
      }
    },
    {
      "kind": "youtube#video",
      "etag": "bYYpT8vYKvx2KgWwIyDlVxxMI9E",
      "id": "KOtA6qCh8Vo",
      "snippet": {
        "publishedAt": "2021-07-16T15:58:04Z",
        "channelId": "UCElGBUWDCa05jRzc2PfmGqQ",
        "title": "Tom MacDonald - \"Withdrawals\"",
        "description": "AUTOGRAPHED ALBUMS & MERCH: http://www.HangOverGang.com\nSUBSCRIBE TO THIS CHANNEL &  CONNECT W/ TOM MACDONALD!\nFACEBOOK: http://www.facebook.com/TomMacDonaldOfficial\nINSTAGRAM: http://www.instagram.com/hangovergang\nTWITTER: http://www.twitter.com/IAmTomMacDonald\nWEBSITE: http://www.hangovergang.com\nSPOTIFY: http://spoti.fi/2H35BQR\niTUNES: https://apple.co/2BQucZO\n\nWRITTEN BY Tom MacDonald\nBEAT PRODUCED BY Tom MacDonald\n\nSHOT and DIRECTED by Nova Rockafeller\nhttp://www.instagram.com/NovaRockafeller\n\nMIXED & MASTERED by Evan Morgan \nhttp://www.evanmorganproductions.com \nhttp://www.youtube.com/user/emorganproductions\nhttp://www.instagram.com/EMorganProductions",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/KOtA6qCh8Vo/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/KOtA6qCh8Vo/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/KOtA6qCh8Vo/hqdefault.jpg",
            "width": 480,
            "height": 360
          },
          "standard": {
            "url": "https://i.ytimg.com/vi/KOtA6qCh8Vo/sddefault.jpg",
            "width": 640,
            "height": 480
          },
          "maxres": {
            "url": "https://i.ytimg.com/vi/KOtA6qCh8Vo/maxresdefault.jpg",
            "width": 1280,
            "height": 720
          }
        },
        "channelTitle": "Tom MacDonald",
        "tags": [
          "Eminem",
          "MGK",
          "Token",
          "NF",
          "Hopsin",
          "Machine Gun Kelly",
          "Merkules",
          "Chris Webby",
          "Joyner Lucas",
          "Tech N9ne",
          "Krizz Kaliko",
          "Yelawolf",
          "Rittz",
          "Strange Music",
          "Slumerican",
          "Jellyroll",
          "Struggle",
          "ICP",
          "Twiztid",
          "Violent J",
          "Shaggy 2 Dope",
          "Upchurch",
          "Adam Calhoun",
          "Ryan Upchurch",
          "Madchild",
          "Logic",
          "Diss Track",
          "Rap Beef",
          "Juggalo",
          "R.A. The Rugged Man",
          "Mac Lethal",
          "Crypt",
          "Quadeca",
          "Horrorcore",
          "Falling In Reverse",
          "Lil Peep",
          "Ghostmane",
          "Pouya",
          "Hip Hop",
          "Rap",
          "Boondox",
          "Country Rap",
          "Tom MacDonald",
          "Whiteboy",
          "mgk",
          "rap battle",
          "freestyle"
        ],
        "categoryId": "10",
        "liveBroadcastContent": "none",
        "localized": {
          "title": "Tom MacDonald - \"Withdrawals\"",
          "description": "AUTOGRAPHED ALBUMS & MERCH: http://www.HangOverGang.com\nSUBSCRIBE TO THIS CHANNEL &  CONNECT W/ TOM MACDONALD!\nFACEBOOK: http://www.facebook.com/TomMacDonaldOfficial\nINSTAGRAM: http://www.instagram.com/hangovergang\nTWITTER: http://www.twitter.com/IAmTomMacDonald\nWEBSITE: http://www.hangovergang.com\nSPOTIFY: http://spoti.fi/2H35BQR\niTUNES: https://apple.co/2BQucZO\n\nWRITTEN BY Tom MacDonald\nBEAT PRODUCED BY Tom MacDonald\n\nSHOT and DIRECTED by Nova Rockafeller\nhttp://www.instagram.com/NovaRockafeller\n\nMIXED & MASTERED by Evan Morgan \nhttp://www.evanmorganproductions.com \nhttp://www.youtube.com/user/emorganproductions\nhttp://www.instagram.com/EMorganProductions"
        },
        "defaultAudioLanguage": "en"
      }
    },
    {
      "kind": "youtube#video",
      "etag": "cw2jZMvkIiPWUpgXTxPUEF-R9ec",
      "id": "TGPzF-HhOkw",
      "snippet": {
        "publishedAt": "2021-07-17T12:46:37Z",
        "channelId": "UCknLrEdhRCp1aegoMqRaCZg",
        "title": "Flooding in Europe kills at least 150 with hundreds still missing | DW News",
        "description": "Record-breaking floods have killed at least 150 people in western Europe. Most of the deaths are in Germany's west - where the disaster area stretches between the towns of Heinsberg, Erftstadt and Ahrweiler, near the border with the Netherlands and Belgium. More than 130 people have been confirmed dead and more than a thousand are still missing. President Frank-Walter Steinmeier has promised support for victims' families, and to the damaged towns.\nIn Belgium, at least 20 people have died in the flooding. The government has declared Tuesday a national day of mourning. \nThe towns of Liège in Belgium and Venlo in the Netherlands have been hit hard. In Venlo 10,000 people were told to evacuate, as well as 200 patients from a hospital. In Liege, the swollen Meuse river has burst.\n\n\nSubscribe: https://www.youtube.com/user/deutschewelleenglish?sub_confirmation=1\n\nFor more news go to: http://www.dw.com/en/\nFollow DW on social media:\n►Facebook: https://www.facebook.com/deutschewellenews/\n►Twitter: https://twitter.com/dwnews\n►Instagram: https://www.instagram.com/dwnews\nFür Videos in deutscher Sprache besuchen Sie: https://www.youtube.com/dwdeutsch\n\n\n#Flooding #Storms #ExtremeWeather",
        "thumbnails": {
          "default": {
            "url": "https://i.ytimg.com/vi/TGPzF-HhOkw/default.jpg",
            "width": 120,
            "height": 90
          },
          "medium": {
            "url": "https://i.ytimg.com/vi/TGPzF-HhOkw/mqdefault.jpg",
            "width": 320,
            "height": 180
          },
          "high": {
            "url": "https://i.ytimg.com/vi/TGPzF-HhOkw/hqdefault.jpg",
            "width": 480,
            "height": 360
          },
          "standard": {
            "url": "https://i.ytimg.com/vi/TGPzF-HhOkw/sddefault.jpg",
            "width": 640,
            "height": 480
          },
          "maxres": {
            "url": "https://i.ytimg.com/vi/TGPzF-HhOkw/maxresdefault.jpg",
            "width": 1280,
            "height": 720
          }
        },
        "channelTitle": "DW News",
        "tags": [
          "DW News"
        ],
        "categoryId": "25",
        "liveBroadcastContent": "none",
        "defaultLanguage": "en-US",
        "localized": {
          "title": "Flooding in Europe kills at least 150 with hundreds still missing | DW News",
          "description": "Record-breaking floods have killed at least 150 people in western Europe. Most of the deaths are in Germany's west - where the disaster area stretches between the towns of Heinsberg, Erftstadt and Ahrweiler, near the border with the Netherlands and Belgium. More than 130 people have been confirmed dead and more than a thousand are still missing. President Frank-Walter Steinmeier has promised support for victims' families, and to the damaged towns.\nIn Belgium, at least 20 people have died in the flooding. The government has declared Tuesday a national day of mourning. \nThe towns of Liège in Belgium and Venlo in the Netherlands have been hit hard. In Venlo 10,000 people were told to evacuate, as well as 200 patients from a hospital. In Liege, the swollen Meuse river has burst.\n\n\nSubscribe: https://www.youtube.com/user/deutschewelleenglish?sub_confirmation=1\n\nFor more news go to: http://www.dw.com/en/\nFollow DW on social media:\n►Facebook: https://www.facebook.com/deutschewellenews/\n►Twitter: https://twitter.com/dwnews\n►Instagram: https://www.instagram.com/dwnews\nFür Videos in deutscher Sprache besuchen Sie: https://www.youtube.com/dwdeutsch\n\n\n#Flooding #Storms #ExtremeWeather"
        },
        "defaultAudioLanguage": "en"
      }
    }
  ]


  },
};
</script>

<style scoped>
</style>