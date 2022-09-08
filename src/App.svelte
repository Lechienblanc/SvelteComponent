<script>
      import Link from './components/Link.svelte'
      import Movable from './components/Movable.svelte'
      import Dialog from "./components/Dialog.svelte";
      import Popover from "./components/Popover.svelte";
      import Select from "./components/Select.svelte";
      import ButtonTerms from './components/ButtonTerms.svelte';
      import SideMenu from './components/SideMenu.svelte';
      import Accordeon from './components/Accordeon.svelte';
      import Slider from './components/Slider.svelte'
      import Radiogroupe from "./components/Radiogroupe.svelte";
      import Todo from "./components/todo.svelte";


      const donne = {
        'Messi': ['etoile',2,3],
        'Lewandowski': [4,5,6,7,8,9,10,11],
        'Henry': [12,24,42]
  }
</script>
<h1>Your components</h1>

<h1>Movable</h1>
<Movable></Movable>

<h1>Link</h1>
<Link 
  leftSideLogo = "https://pbs.twimg.com/profile_images/1498367008789905413/C61plwJx_400x400.jpg"
  rightSideLogo = ""
  title = "Nomad twitter"
  link ='https://twitter.com/Nomad_eSport'
  backgroundcolor = 'blue'>
</Link>

<h1>Dialog</h1>
<Dialog></Dialog>

<h1>Popover</h1>
<Popover></Popover>

<h1>Select</h1>
<Select></Select>

<h1>SideMenu</h1>
<SideMenu 
    titre1 = "Hetic"
    titre2 = "Vert"
    titre3 = "Bleu"
    titre4 = "Jaune"

    article_titre1 = 'Hetic - École du numérique'
    article_titre2 = 'Texte en vert'
    article_titre3 = 'Texte en bleu'
    article_titre4 = 'Texte en jaune'

    article_content1 = 'La Tech est désormais la voie royale vers les plus belles opportunités de carrière : toutes les entreprises, de toutes tailles et de tous secteurs, recrutent des talents au service de leur transformation digitale.'
    article_content2 = 'Appuyez sur le bouton pour passer le texte en vert.'
    article_content3 = 'Appuyez sur le bouton pour passer le texte en bleu.'
    article_content4 = 'Appuyez sur le bouton pour passer le texte en jaune.'

    article_img1 = 'https://learn.hetic.net/branding/_168_1/loginLogo/CustomLoginLogo.png?m=kmkwxem4'
/>

<h1>buttonTerms</h1>
<ButtonTerms
    texte_checkbox = 'Accepter les termes et conditions'
/>

<h1>Slider</h1>
<Slider></Slider>

<h1>Radiogroupe</h1>
<Radiogroupe sport = {[
  { label: 'foot'},
  { label: 'basket'},
  { label: 'golf'}
]}>
</Radiogroupe>

<h1>Accordeon</h1>
{#each Object.entries(donne) as entry}
<Accordeon {entry} />
{/each}

<h1>TodoList</h1>
<Todo></Todo>

