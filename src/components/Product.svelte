<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: [
        "Daily streak counter",
        "Weights and reps tracker",
        "Community challenges",
        "Every workout is new and exciting",
      ],
      description:
        "Swoley moley ensures all users have the information they need to train safely and train effectively.",
      imgUrl: "",
    },
    {
      featureList: [
        "Slect your preferences",
        "Personalise your workouts",
        "Customise your training",
        "Guarentees progress on all core exercises",
      ],
      description:
        "Build ytour streaks anbd see your progress with our amazing tracking and analytics features.",
      imgUrl: "",
    },
    {
      featureList: [
        "Eliminating guesswork",
        "Save time",
        "Load your own models",
        "Achieve the performance you seek",
        "Builds functional strength",
      ],
      description:
        "Enter as much information about yourself as you desire to ensure all workouts are personalised to your ever need.",
      imgUrl: "",
    },
  ];
</script>

<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your lifetime <span class="text-indigo-400">gym steak</span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] max-auto w-full font-semibold text-center"
      >
        Features for everyone
      </h3>
    </div>
    <div
      class="grid grid-cols-1 md:grid-col-2 gap-14 md:gap-14 lg:gap-20 relative text-base"
    >
      {#each productFeatures as productFeature, index}
        <ProductCard {productFeature} {index}>
          {#if index === 0}
            Experience a beginner exercise <span
              class="text-indigo-400 font-medium">class</span
            >
          {:else if index === 1}
            Lay the foundations for <span class="text-indigo-400 font-medium"
              >routine</span
            ><br /> and consistency
          {:else}
            Workouts specific to your <span class="text-indigo-400 font-medium"
              >environemnt</span
            >
            and <span class="text-indigo-400 font-medium">expertise</span>
          {/if}
        </ProductCard>
      {/each}
    </div>
  </div>
</SectionWrapper>
