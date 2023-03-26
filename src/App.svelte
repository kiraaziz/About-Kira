<script>
    import Contact from "./components/Contact.svelte";
import Know from "./components/Know.svelte";
import Main from "./components/Main.svelte";
    import Me from "./components/Me.svelte";
    import Navbar from "./components/Navbar.svelte"
    import Projects from "./components/Projects.svelte";
    import Screen from "./components/Screen.svelte";

</script>
<svelte:head>
    <title>Rj Aziz : Kira</title>
    <meta name="theme-color" content="#111827"/>
    <link rel="icon" href="/images/show.gif" />
</svelte:head>
<Screen>
    <Navbar />
    <Main>
        <Me />
        <Know />
        <Projects />
        <Contact />
    </Main>
</Screen>