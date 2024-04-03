<script lang="ts">
	import {
		Page,
		Navbar,
		Block,
		Button,
		List,
		ListItem,
		Link,
		BlockTitle,
		Panel
	} from 'konsta/svelte';

	import { Menu, X } from 'lucide-svelte';

	let count: number = 0;
	let leftPanelOpened = false;

	function onCoubt() {
		count += 1;
	}
</script>

<Page>
	<Navbar title="SG2T">
		<Link slot="left" navbar onClick={() => (leftPanelOpened = true)} class="p-2">
			<Menu class="text-white" />
		</Link>
	</Navbar>

	<BlockTitle>Navegação</BlockTitle>
	<List>
		<ListItem href="/about" title="Sobre" />
	</List>
	<Block strong>
		<p>Sistema de Geolocalização e gerenciamento de Tarrenos</p>
	</Block>

	<Block strong class="flex space-x-4">
		<Button onClick={onCoubt}>Clicke Aqui {count ? count : ''}</Button>
	</Block>

	<Panel side="left" opened={leftPanelOpened} onBackdropClick={() => (leftPanelOpened = false)}>
		<Page>
			<Navbar title="SG2T">
				<Link slot="right" navbar onClick={() => (leftPanelOpened = false)}>
					<X class="text-white w-4 h-4"></X>
				</Link>
			</Navbar>
			<Block class="space-y-4">
				<p>SG2T</p>
			</Block>
		</Page>
	</Panel>
</Page>
