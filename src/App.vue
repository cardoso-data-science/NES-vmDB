  <!-- App.vue -->
  <template>
    <div id="app">
      <section> 
        <div class="header">
            <h1>The NES Video-Music Database: A Dataset of Symbolic Video Game Music Paired with Gameplay Videos</h1>
            <<h1>NES-vmDB</h1>
            <div >
              <a href="https://www.linkedin.com/in/igor-rodriguescardoso/">
                  Igor R. Cardoso<sup>1</sup>
              </a>
              <a href="https://github.com/rubensolv">
                  Rubens O. Moraes<sup>1</sup>
              </a>
              <a href="https://github.com/lucasnfe/">
                  Lucas N. Ferreira<sup>1</sup>
              </a>
            </div>
            <div >
              <a href="https://ppgcc.ufv.br/">
                <sup>1</sup>Universidade Federal de Viçosa
              </a>
          
            </div>
        </div>
      </section>
  
      <!-- <div class="header" style="font-family: 'Press Start 2P', cursive;">
          <h1>NES-mvDB</h1>
      </div> -->


      <!-- Text with Title -->
      <section>
        <div class="project-icons">
            <a href="https://arxiv.org/pdf/2006.16236.pdf">
                <i class="fa fa-file"></i> <br>
                Paper
            </a>
            <a href="https://colab.research.google.com/drive/1BV4OaWRAHYGeimO0cqHD86GfnfgUaKD4?usp=sharing">
                <img src="C:\Users\igor.r.cardoso\workspace\nesmvdb-webpage\nesmvdb-webpage\src\imgs\colab_logo.png" style="width: 35px;"> <br>
                Colab
            </a>
            <a href="https://github.com/idiap/fast-transformers">
                <i class="fa fa-github"></i> <br>
                Code
            </a>
            <a href="https://fast-transformers.github.io">
                <i class="fa fa-book"></i> <br>
                Docs
            </a>
            <a href="https://youtu.be/KBWh7XCUAi8">
                <i class="fa fa-youtube-play"></i> <br>
                Video
            </a>
            <a href="http://idiap.ch/~katharas/pdfs/linear-transformers-slides.pdf">
                <i class="fa fa-file-powerpoint-o"></i> <br>
                Slides
            </a>
        </div>
        
        
        <h2>O que é o NES-vmDB?</h2>
        <p>Um banco de dados que mapeia trechos de gameplayes de jogos NES
           para suas trilhas sonoras originais.</p>
        <p>O NES-mvDB é construído por uma lógica bem conhecida, mas aplicada a um contexto nunca antes explorado.
          Utilizando uma técinica analoga ao famoso sistema Shazam isolamos os audios de centenas de gameplays e
          mapeamos para a trilha sonora original.</p>
        <p>
          O processo de criação da base é mais bem descrito no nosso artigo, https://arxiv.org/abs/2404.04420
        </p>
        
        <h2>A equipe</h2>
        <p>Somos pioneiros com os trabalhos de criatividade computacional na Universiade Federal de Viçosa,
           tendo este trabalho como nosso ponta pé inicial e ponto de partida para os próximos grandes trabalhos.</p>
      </section>
      <!-- Two Columns Layout -->
      <h2>Resultados</h2>

      <section class="two-columns">
        
        <!-- Left Column with Video Player -->
        <div class="left-column">
          <video-player :video-source="videoSource1" />
        </div>
        
        <!-- Right Column with Music Player -->
        <div class="right-column">
          <music-player :music-source="musicSource1" />
        </div>
      </section>
      <section class="two-columns">
        
        <!-- Left Column with Video Player -->
        <div class="left-column">
          <video-player :video-source="videoSource2" />
        </div>
        
        <!-- Right Column with Music Player -->
        <div class="right-column">
          <music-player :music-source="musicSource2" />
        </div>
      </section>
      <section class="two-columns">
        
        <!-- Left Column with Video Player -->
        <div class="left-column">
          <video-player :video-source="videoSource3" />
        </div>
        
        <!-- Right Column with Music Player -->
        <div class="right-column">
          <music-player :music-source="musicSource3" />
        </div>
      </section>
      <h2>How to cite?</h2>
      <p>If you use the NES-vmDB dataset in your work, please cite the paper where it was introduced:</p>
      <div class="highlight"><pre class="highlight"><code>Igor R. Cardoso, Rubens O. Moraes and Lucas N. Ferreira. "The NES
Video-Music Database: A Dataset of Symbolic Video Game Music Paired with Gameplay Videos."
  In Foundations of Digital Games, 2024.
</code></pre></div>
      <p>You can also use the following BibTeX entry:</p>
      <pre class="highlight"><code>@inproceedings{
  hawthorne2018enabling,
  title={The NES Video-Music Database: A Dataset of Symbolic Video Game Music Paired with Gameplay Videos.},
  author={Igor R. Cardoso and Rubens O. Moraes and Lucas N. Ferreira},
  booktitle={Foundations of Digital Games},
  year={2024},
  url={https://arxiv.org/abs/2404.04420},
}
</code></pre>
    </div>
  </template>

  <script>
  import VideoPlayer from './components/VideoPlayer.vue';
  import MusicPlayer from './components/MusicPlayer.vue';

  export default {
    name: 'App',
    components: {
      VideoPlayer,
      MusicPlayer
    },
    data() {
      return {
        videoSource1: 'src\\components\\videos\\322_segment_21.mp4',
        musicSource1: 'src\\components\\musics\\322_SuperMarioBros__00_01RunningAbout.mp3',
        videoSource2: 'src\\components\\videos\\348_segment_193.mp4',
        musicSource2: 'src\\components\\musics\\348_TheLegendofZelda_01_02OverworldBGM.mp3',
        videoSource3: 'src\\components\\videos\\048_segment_8.mp4',
        musicSource3: 'src\\components\\musics\\045_Castlevania_01_02VampireKiller.mp3'
      };
    }
  }
  </script>

  <style>

  .project-icons {
      text-align: center;
      margin-bottom: 30px;
      display: block;
      align-content: center
  }
  .fa {
    display: inline-block;
    font: normal normal normal 14px / 1 FontAwesome;
    font-size: inherit;
    text-rendering: auto;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
} 
  @font-face {
    font-family: 'PixeledFont';
    src: url('path/to/your/pixelated-font.ttf') format('truetype');
  }

  /* Apply the pixelated font to the header */
  /* CSS for two-columns layout */
  .two-columns {
    display: flex;
  }

  .left-column {
    flex: 1;
    /* padding: 20px; */
    align-content: center;    
  }
  .right-column {
    flex: 1;
    /* padding: 20px; */
    align-content: center;
  }

  /* CSS for header */
  .header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #682a2c;
  text-align: center;
  padding: 20px 0;
  height: 200px;
  /* display: flex; */
  /* justify-content: baseline; */
  /* align-items: center; */
  /* display: block; */
}
.markdown-body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    font-size: 16px;
    line-height: 1.5;
    word-wrap: break-word;
}

h2 {
  margin-top: 20px;
}


.header h1 {
  margin: 0;
  color: #ffffff; /* Dark color for contrast */
  font-size: 32px;
  font-weight: bold; /* Making text bold */
  font-family: 'PixeledFont', sans-serif;

}
pre, code {
    font-size: inherit;
    border: 1px solid #e8e8e8;
    border-radius: 3px;
    background-color: #f2e6ec;
    margin-top: 20px;
    margin-bottom: 20px;
}
  </style>
