<script lang="ts">
    interface Props {
        image: string;
        title: string;
        description: string;
        gallery?: string;
    }

    let props: Props = $props();
</script>

<div class="aspect-square overflow-hidden">
    <a href={props.image} class="glightbox"
        data-gallery={props.gallery || "abcd"}
        data-title={props.title}
        data-description={props.description}
        data-effect="fade"
        data-zoomable="false"
        data-draggable="false"
    >
        <img class="w-full h-full object-cover object-center" src={props.image} alt={props.title} />
    </a>
</div>
