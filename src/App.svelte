<script>
	import Entry from './Entry.svelte';

	let words = [
				{key: "a", val: "signifies emphasis, emotion or confirmation"}, 
				{key: "kin", val: "signifies emphasis, emotion or confirmation"},
				{key: "akesi", val: "amphibious, reptilian, non-cute animal"},
				{key: "ala", val: "no, nothing, not, zero"},
				{key: "alasa", val: "hunt, forage"},
				{key: "ale", val: "everything, all, countless, bountiful, abundant, life, universe, 100"},
				{key: "ali", val: "everything, all, countless, bountiful, abundant, life, universe, 100"},
				{key: "anpa", val: "downward, humble, lowly, dependent, defeat"},
				{key: "ante", val: "change, altered, other, different"},
				{key: "anu", val: "or"},
				{key: "awen", val: "endure, keep, protect, safe, wait, stay, continue"},
				{key: "e", val: "(marks the direct object)"},
				{key: "en", val: "(placed between multiple subjects)"},
				{key: "esun", val: "market, shop, bazaar, trade, transaction"},
				{key: "ijo", val: "thing, action, object, matter"},
				{key: "ike", val: "bad, negative, complex, non-essential, irrelevant"},
				{key: "ilo", val: "tool, implement, machine"},
				{key: "insa", val: "center, content, inside, between, organ"},
				{key: "jaki", val: "disgusting, unclean"},
				{key: "jan", val: "person, someone"},
				{key: "jelo", val: "yellow"},
				{key: "jo", val: "have, carry, contain, hold"},
				{key: "kala", val: "fish, marine animal"},
				{key: "kalama", val: "produce a sound"},
				{key: "kama", val: "arrive, come, future, become, achieve, succeed"},
				{key: "kasi", val: "plant, vegetation, herb, leaf"},
				{key: "ken", val: "can, may, possible"},
				{key: "kepeken", val: "use, using"},
				{key: "kili", val: "fruit, vegetable, edible plant"},
				{key: "kiwen", val: "hard substance or object, metal, rock"},
				{key: "ko", val: "clay, dough, paste, powder"},
				{key: "kon", val: "air, breath, spirit, hidden"},
				{key: "kule", val: "colour, pigment, paint"},
				{key: "kulupu", val: "community, group, society"},
				{key: "kute", val: "ear, hear, listen, obey"},
				{key: "la", val: "(between a context phrase and the main sentence)"},
				{key: "lape", val: "sleep, rest"},
				{key: "laso", val: "blue, green"},
				{key: "lawa", val: "head, mind, control, lead, own, plan, rule"},
				{key: "len", val: "cloth, clothing, cover, layer"},
				{key: "lete", val: "cold, cool, raw"},
				{key: "li", val: "(predicate marker, not used when mi or sina is the subject)"},
				{key: "lili", val: "small, littl, short, few, young"},
				{key: "linja", val: "long and flexible thing, string, hair, rope"},
				{key: "lipu", val: "flat object, book, document, paper, record, website"},
				{key: "loje", val: "red"},
				{key: "lon", val: "at, real, true, exist"},
				{key: "luka", val: "arm, hand, tactile limb, five"},
				{key: "lukin", val: "eye, look at, see, examine, observe, read, watch, search, try"},
				{key: "oko", val: "eye, look at, see, examine, observe, read, watch, search, try"},
				{key: "lupa", val: "door, hole, orifice, window"},
				{key: "ma", val: "earth, land, outdoors, territory, soil"},
				{key: "mama", val: "parent, ancestor, creator, caretaker"},
				{key: "mani", val: "money, wealth, large domesticated animal"},
				{key: "meli", val: "woman, female, feminine, wife"},
				{key: "mi", val: "i, me, we, us (first person pronoun)"},
				{key: "mije", val: "man, male, masculine, husband"},
				{key: "moku", val: "eat, drink, swallow"},
				{key: "moli", val: "dead, death, die"},
				{key: "monsi", val: "back, behind"},
				{key: "mu", val: "animal noise"},
				{key: "mun", val: "moon, star, night sky object"},
				{key: "musi", val: "artistic, fun, play, frivolous"},
				{key: "mute", val: "many, a lot, more, several, many, quantity"},
				{key: "nanpa", val: "number, (marks ordinal number)"},
				{key: "nasa", val: "unusual, strange, foolish, silly, drunk"},
				{key: "nasin", val: "way, path, road, custom, doctrine, method"},
				{key: "nena", val: "bump, button, hill, mountain, nose, protuberance"},
				{key: "ni", val: "this, that, (demonstrative)"},
				{key: "nimi", val: "name, word"},
				{key: "noka", val: "foot, leg, moving organ, bottom, lower part"},
				{key: "o", val: "hey!, (marks vocative or imperative)"},
				{key: "olin", val: "love, have compassion for, respect, show affection to"},
				{key: "ona", val: "he, she, they, (third person pronoun)"},
				{key: "open", val: "begin, start, open, switch on"},
				{key: "pakala", val: "break, damage, harm"},
				{key: "pali", val: "do, action, work, build, make, prepare"},
				{key: "palisa", val: "long hard thing, branch, rod, stick"},
				{key: "pan", val: "cereal, grain, rice, wheat, bread, pasta, gluten-based food"},
				{key: "pana", val: "give, send, emit, provide, put, release"},
				{key: "pi", val: "(indicates that the following noun phrase describes the former one)"},
				{key: "pilin", val: "heart, feel, emotion, experience"},
				{key: "pimeja", val: "black, dark, unlit"},
				{key: "pini", val: "complete, end, finish, past"},
				{key: "pipi", val: "insect"},
				{key: "poka", val: "side, hip, next to, nearby, vicinity"},
				{key: "poki", val: "container"},
				{key: "pona", val: "good, positive, simple, useful, friendly, peaceful"},
				{key: "pu", val: "interact with the official toki pona book"},
				{key: "sama", val: "same, similar, each other, peer, fellow"},
				{key: "seli", val: "fire, ingredient, chemical reaction, heat source"},
				{key: "selo", val: "outer layer, bark, peel, shell, skin, boundary"},
				{key: "seme", val: "what, which"},
				{key: "sewi", val: "above, highest, elevated, divine, sacred, supernatural, sky"},
				{key: "sijelo", val: "body, health, torso"},
				{key: "sike", val: "round or circular, sphere, circle, cycle, loop, wheel, year"},
				{key: "sin", val: "new, fresh, additional, another"},
				{key: "namako", val: "new, fresh, additional, another"},
				{key: "sina", val: "you, (second person pronoun)"},
				{key: "sinpin", val: "front, face, foremost, wall"},
				{key: "sitelen", val: "image, representation, symbol, mark, writing"},
				{key: "sona", val: "know, skill, wise, information, think"},
				{key: "soweli", val: "land animal, beast"},
				{key: "suli", val: "big, tall, important, adult"},
				{key: "suno", val: "sun, light, shine, light source"},
				{key: "supa", val: "horizontal surface or object, object to rest something on, seat"},
				{key: "suwi", val: "sweet, cute, innocent"},
				{key: "tan", val: "by, from, because"},
				{key: "taso", val: "but, however, only"},
				{key: "tawa", val: "go, toward, for, from the perspective of, move"},
				{key: "telo", val: "water, liquid, fluid, wet substance, drink"},
				{key: "tenpo", val: "time, duration, moment, occasion, period, situation"},
				{key: "toki", val: "communicate, say, speak, talk, use language, hello"},
				{key: "tomo", val: "indoor space, building, home, house, room"},
				{key: "tu", val: "two"},
				{key: "unpa", val: "sex, have sex with"},
				{key: "uta", val: "mouth, lips, jaw, kiss"},
				{key: "utala", val: "battle, challenge, compete, struggle"},
				{key: "walo", val: "white, pale, light coloured"},
				{key: "wan", val: "unique, united, one"},
				{key: "waso", val: "bird, flying creature"},
				{key: "wawa", val: "strong, powerful, confident, sure, energetic, intense"},
				{key: "weka", val: "absent, away, ignored"},
				{key: "wile", val: "must, need, require, should, want, wish"},
			];
	let input = '';
	let mode = "toki pona";

	document.addEventListener('keydown', function(event) {
		if (event.key == "Enter") {
			if (mode == "toki pona") {
				mode = "english"
			}
			else {
				mode = "toki pona"
			}
		}
	});
</script>

<main>
	<h1>lipu pi nimi ale pi toki pona</h1>
	<i>Toki Pona Dictionary</i>

	<div style="padding: 50px">
	
	<input bind:value={input}>
	
	<div style="padding: 30px">

	<p>currently searching for <i style="background: #121212; color: #F5F5F5; font-style: normal;">{mode}</i> words, press <i style="background: #121212; color: #F5F5F5; font-style: normal;">enter</i> to change the search language.</p>
	
	<div style="padding: 30px">
	
	<div style="display: inline-block; text-align: left;">
		{#each words as {key, val}}
			{#if !input.match(/^[0-9a-z]+$/)}
				<Entry key={key} value={val}/>
			{:else if input && mode == "toki pona" && key.includes(input)}
				<Entry key={key} value={val}/>
			{:else if input && mode == "english" && val.includes(input)}
				<Entry key={key} value={val}/>
			{/if}
		{/each}
	</div>
</main>