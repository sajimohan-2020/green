<script lang="ts">
  import { PUBLIC_APIURL } from "$env/static/public";
  import Faq from "$lib/components/faq/Faq.svelte";
  import { conditionFaqs, items } from "$lib/components/data/assets";
  import Bookmarknav from "$lib/components/bookmarknav/BookMarkNav.svelte";
  import Whycondition from "./WhyCondition.svelte";
  import Explore from "$lib/components/ui/explore/Explore.svelte";
  import Heading from "$lib/components/heading/Heading.svelte";
  import P from "$lib/components/paragraph/Paragraph.svelte";
  import OurService from "./OurService.svelte";
  import WhyChoose from "./WhyChoose.svelte";
  import Calltoaction from "./CallToAction.svelte";
  import IndustriesSection from "./IndusriesSection.svelte";
  import Thickline from "$lib/icons/svgs/thickline.svelte";
  import Vibrationanalysis from "../../servicedetails/[id]/+page.svelte";
  import Infraredthermography from "../../subservices1/[id]/+page.svelte";
  import Ultrasonic from "../../subservices2/[id]/+page.svelte";
  import Oilanalysis from "../../subservices3/[id]/+page.svelte";
  import Pipingvibration from "../../subservices5/[id]/+page.svelte";
  import Motorcurrent from "../../subservices6/[id]/+page.svelte";
  import Structuralvibration from "../../subservices10/[id]/+page.svelte";
  import Ods from "../../subservices17/[id]/+page.svelte";
  import Partialdischarge from "../../subservices7/[id]/+page.svelte";
  import Powerharmonic from "../../subservices18/[id]/+page.svelte";
  import Earthpittesting from "../../subservices8/[id]/+page.svelte";
  import Insulationresistance from "../../subservices19/[id]/+page.svelte";
  import Windingresistance from "../../subservices20/[id]/+page.svelte";
  import Tandelta from "../../subservices16/[id]/+page.svelte";
  import Partialdischargemonitoring from "../../subservices23/[id]/+page.svelte";
  import Cfd from "../../subservices14/[id]/+page.svelte";
  import Finite from "../../subservices15/[id]/+page.svelte";
  import Compressed from "../../subservices21/[id]/+page.svelte";
  import Flowmeasurement from "../../subservices22/[id]/+page.svelte";
  import Steamtrap from "../../subservices9/[id]/+page.svelte";
  import Ens from "../../subservices24/[id]/+page.svelte";
  import Lightservices from "../../subservices13/[id]/+page.svelte";
  import Insitu from "../../subservices11/[id]/+page.svelte";
  import LaserShaft from "../../subservices12/[id]/+page.svelte";
  import Performance from "../../subservices4/[id]/+page.svelte";

  /** @type {import('./$types').PageData} */

  export let data;
  let isOpen = false;

  interface name {
    title: string;
    text?: string;
  }
  const name: name[] = [
    {
      title:
        " Partner with assetconditionmonitoring for reliable, predictive solutions.",
      text: "Lets talk",
    },
  ];
</script>

<!-- src="{PUBLIC_APIURL}/assets/{data.services.banner_image}" -->
{#if data?.services?.translations?.[0]?.title?.includes("Condition Monitoring Services")}
  <div class="pt-24 sm:pt-28 lg:pt-28">
    <div class="flex items-center justify-center relative">
      <img
        src={`${PUBLIC_APIURL}/assets/${data.services.banner_img}`}
        alt="condition-monitoring-services"
        class="w-full h-[300px] md:h-[300px] lg:h-[450px] object-cover object-right"
      />
      <div class="absolute left-[2%] w-fit h-auto">
        <div class="flex items-center gap-1 h-[50px] md:h-[70px]">
          <Thickline data="w-[1.5rem] md:w-[3rem] h-20px" />
          <Heading size="headingH3" className=" font-bold text-white ">
            {data?.services?.translations?.[0]?.title}
          </Heading>
        </div>
      </div>
    </div>
  </div>
  <Bookmarknav bgColor="bg-[#F7FAFE]" textcolor="text-[#777777]" {items} />
  <div class="flex flex-col items-center justify-center gap-8">
    <Whycondition />
    <Explore {name} width="w-[90%]" data={`/${data.langParam}/contactus`} />
    <div class="container mx-auto px-5 md:px-[55px] mt-16">
      <Heading size="bannerMaih1" className="text-[#1846A3] mb-6 text-left ">
        What is Condition Monitoring and Why Does It Matter?
      </Heading>
      <P size="texts18" className="text-gray-700 leading-relaxed mb-8">
        Track equipment health in real time using smart sensors to measure
        vibration, temperature, and pressure. Regular monitoring turns
        maintenance into a strategic advantage — cutting costs, preventing
        failures, and boosting performance. At AssetConditionMonitoring, we make
        condition monitoring easy with smart, efficient solutions that keep your
        operations running safely and smoothly.
      </P>
    </div>
    <OurService {data} />
    <IndustriesSection />
    <WhyChoose />
    <div class="container mx-auto px-5 md:px-[55px]">
      <h2
        class="text-[#1846A3] text-xl font-bold capitalize
font-style: italic"
      >
        "Stay ahead with smarter,faster and more accurate monitoring. Partner
        with us today for smarter, more efficient maintenance solutions."
      </h2>
    </div>
    <Faq faqs={conditionFaqs} />
    <!-- <Calltoaction /> -->
  </div>
{/if}

{#if data?.services?.translations?.[0]?.title?.includes("Machinery Vibration Analysis")}
  <Vibrationanalysis {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Infrared Thermography Testing")}
  <Infraredthermography {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Ultrasonic Inspection")}
  <Ultrasonic {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Lube Oil Analysis")}
  <Oilanalysis {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Piping Vibration Analysis")}
  <Pipingvibration {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Motor Current Signature Analysis")}
  <Motorcurrent {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Structural Vibration Analysis")}
  <Structuralvibration {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("ODS and Modal Analysis")}
  <Ods {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Partial Discharge Testing")}
  <Partialdischarge {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Power Quality & Harmonic Analysis")}
  <Powerharmonic {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Earth Pit Testing")}
  <Earthpittesting {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Insulation Resistance & Polarization Index")}
  <Insulationresistance {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Winding Resistance Measurement")}
  <Windingresistance {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Tan-Delta and Capacitance Measurement")}
  <Tandelta {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Partial Discharge Measurement")}
  <Partialdischargemonitoring {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Computational Fluid Dynamics (CFD)")}
  <Cfd {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Finite Element Analysis (FEA)")}
  <Finite {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Compressed Air Leak Detection Services")}
  <Compressed {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Flow Measurement Services")}
  <Flowmeasurement {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Steam Trap Testing")}
  <Steamtrap {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Environmental Noise Survey")}
  <Ens {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Light Survey")}
  <Lightservices {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("In-situ Dynamic Balancing")}
  <Insitu {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Laser Shaft Alignment")}
  <LaserShaft {data} />
{/if}
{#if data?.services?.translations?.[0]?.title?.includes("Performance Testing & Analysis of Pumps and Compressors")}
  <Performance {data} />
{/if}
