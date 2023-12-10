<script lang="ts">
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import TopBar from '$lib/TopBar.svelte';
	import Posts from '$lib/Posts.svelte';
	export let data: { posts: { path: string; meta: { title: string; date: string } }[] };
</script>

<TopBar {data} />
{#if browser}
	<Carousel
		timingFunction="linear"
		swiping={false}
		arrows={false}
		dots={false}
		autoplay={true}
		autoplayDuration={5000}
	>
		<img src="/carousel0.jpg" alt="colourful mountains" />
		<img src="/carousel1.jpg" alt="dark and raining" />
	</Carousel>
{/if}
<div id="content">
	<h1>Brothers International Community</h1>
	<h2>Join brothers community</h2>
	<h3>Build trustworthy international connections</h3>
	<Posts posts={data.posts} />
	<div id="summary">
		<p>
			We are a group of Brothers, who created this community and selfishly named it after the
			brotherly relationship we share.
		</p>

		<p>
			First of all, ‘Brothers’ is considered a gender neutral term in our community, man or woman,
			you’re equal in our community. We use this single term to represent all of us regardless of
			our gender, ethnicity and any other differences. We believe that the gender neutral word also
			filters away any undesirable gender attraction it may cause, thus creating a pure relationship
			of family we can trust and feel safe upon while amongst strangers.
		</p>

		<p>
			We’ve always dreamt to create a community of trustworthy people working together and helping
			each other out. But we realised that in this hectic world, everyone is out for themselves and
			not many are interested in building relationships that doesn’t benefit them somehow.
		</p>

		<p>
			Tasting the sweetness of this camaraderie, we understood how hard it is to build such bonds.
		</p>

		<p>
			People tend to forget that they’re amassing wealth and positions for happiness and peace in
			life. While our community believes that true happiness and peace in life exists due to the
			people who really cares for us around us. Thus building good people to live together with is
			also essential for us to remain happy just as much as how we need wealth and status.
		</p>

		<p>
			In practical life many are forced to abandon their good relationships afraid that they won’t
			benefit from it in the long run. We abandon people who were once very close to us because they
			aren’t equal to us anymore. Slowly we learn to build relations only due to the benefits they
			provide. Relationships become a trade of benefits rather than the genuine warmth they’re
			supposed to provide.
		</p>

		<p>
			While forsaking the relationships that don’t benefit us, we gradually grow selfish and are
			bothered about our life alone. And we slowly learn to relinquish our childhood innocence and
			the genuine concern we felt for the people around us. Our life gradually narrows down to a
			singular unit of ourselves, unable to gain back the ability to give warmth to others and to
			recieve it from others.
		</p>

		<p>
			Our dream is to create a community of Brothers who are genuine to each other and retain this
			warmth and concern between themselves so that all of us can live a content and peaceful life
			within such bonds.
		</p>

		<p>
			We believe that the majority of the people who join this community and seek it’s services may
			only look for their own personal benefits. Yet we created this platform as an initiation where
			we may meet people of similar interests, true Brothers who can work together and help each
			other out. Such bonds are more precious than any wealth we make. Creating such bonds require
			lots of effort by an individual. Thus we use this community as a medium to earn such people
			and bonds, to make a large web of people of such similar interests.
		</p>

		<p>
			Even finding a couple dozen sincere Brothers from the millions of members we may potentially
			acquire, shall fulfill our honest dream. Our community was solely created to find those couple
			dozen group of people.
		</p>

		<p>
			I believe nothing in this world can destroy the bonds of such a group of people. People of the
			pure heart, devoid of jealousy, selfishness, envy and pride amongst each other. People who
			show genuine brotherly concern for each other. People who are ready to adjust with others and
			don’t dominate others with their ego. People who don’t keep grudges towards each other. People
			who don’t trample others for their own personal status and ambitions.
		</p>

		<p>
			We hope that our initiation may rekindle the warmth and concern buried in people’s heart for
			one another and they soon reach out to each other as real brothers.
		</p>

		<p>
			We look forward to the future, concealed by a veil of fate and believe that our dream shall be
			fulfilled one day.
		</p>

		<p>~Brothers Team.</p>
	</div>
</div>

<footer>
	<div id="contact">
		<a href="mailto:brotherscommunityinternational@gmail.com">
			<img src="/email.svg" alt="email" width="50px" /></a
		>
		<a href="https://t.me/Brothers_in_law"
			><img src="/telegram.svg" alt="telegram" width="50px" /></a
		>
	</div>
</footer>

<style>
	h1 {
		color: #8fbcbb;
	}
	h2 {
		color: #88c0d0;
	}
	h3 {
		color: #81a1c1;
	}
	img {
		border-radius: 0.5rem;
	}
	#content {
		text-align: center;
	}
	#summary {
		text-align: left;
		margin: 1em;
	}
	#contact {
		display: flex;
		justify-content: space-around;
	}
</style>
