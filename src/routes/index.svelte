<script>
  import Dialog from "../components/Dialog.svelte";
//   import User from "../components/User.svelte";
  const toto = ["toto", "toto.jpeg"]
  const lili = ["lili", "lili.jpeg"]
  const zozo = ["zozo", "zozo.jpeg"]
  const tux = ["tux", "tux.jpeg"]
  const foo = ["foo", "foo.jpeg"]
  const anonymous = ["anonymous", "anonymous.png"]
  const dialog = [
    {
      user: toto,
      said: "hello there",
      interloc: true,
      answers: [
        {
          interloc: true,
          user: lili,
		  said: "hey, how are U?",
		  answers: [
			  {
				  user: toto,
				  said: "fine and you?"
			  },
			  {
				  user: zozo,
				  said: "hello you two!",
				  interloc: true,
				  answers: [
					  {user: lili, said: "hey zozo!"},
					  {user: toto, said: "how are you zozo?"},
					  {user: tux, said: "glad to see you zozo.", interloc: true, answers: [
						  {
							  user: zozo, said: "hey tux, thank god you're there too! so what's new"
						  }
					  ]}
				  ]
			  },
		  ]
        },
      ],
    },
    {
      interloc: true,
      user: anonymous,
	  said: "is there anybody out there?",
	  answers: [
		  {user: foo, said: "nope"}
	  ],
    },
  ];
//   console.log(dialog)
</script>
{#each dialog as sentence}
	<div class="frame">
		 <!-- content here -->
		 <Dialog {sentence} />
		</div>
	{/each}

<style>
	.frame{
		border: 1px solid #444;
		border-radius: 5px;
		margin: 1rem;
	}
</style>
