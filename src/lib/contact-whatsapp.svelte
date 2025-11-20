<script lang="ts">
    interface Props {
        text: string;
    }

    const props: Props = $props();
    const phone = '400769194863';

    const onclick = () => {
        const url = `https://wa.me/${phone}?text=${encodeURIComponent(props.text)}`;
        window.open(url, '_blank', 'noopener');
    }
</script>

<a
    class="text-lg text-lime-600"
    href="#"
    target="_blank"
    rel="noopener noreferrer"
    aria-label="Contacteaza-ma pe WhatsApp"
    {onclick}
>
    <i class="fa-brands fa-whatsapp"></i>
    Contactează-mă pe WhatsApp
</a>
