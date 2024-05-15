<script lang="ts">
	import { Badge } from '$lib/components/ui/badge/index.js';
	import { Button } from '$lib/components/ui/button/index.js';
	import * as Card from '$lib/components/ui/card/index.js';
	import * as DropdownMenu from '$lib/components/ui/dropdown-menu/index.js';
	import { Input } from '$lib/components/ui/input/index.js';
	import { Label } from '$lib/components/ui/label/index.js';
	import * as Pagination from '$lib/components/ui/pagination';
	import * as Table from '$lib/components/ui/table/index.js';
	import * as Tabs from '$lib/components/ui/tabs/index.js';
	import { Textarea } from '$lib/components/ui/textarea/index.js';
	import CircleUser from 'lucide-svelte/icons/circle-user';

	import Activity from 'lucide-svelte/icons/activity';
	import Banknote from 'lucide-svelte/icons/banknote';
	import CalendarPlus from 'lucide-svelte/icons/calendar-plus';
	import CalendarClock from 'lucide-svelte/icons/calendar-clock';
	import Coins from 'lucide-svelte/icons/coins';
	import CreditCard from 'lucide-svelte/icons/credit-card';
	import Home from 'lucide-svelte/icons/home';
	import ListTodo from 'lucide-svelte/icons/list-todo';
	import Logout from 'lucide-svelte/icons/log-out';
	import Pencil from 'lucide-svelte/icons/pencil';
	import Save from 'lucide-svelte/icons/save';
	import ScrollText from 'lucide-svelte/icons/scroll-text';
	import Search from 'lucide-svelte/icons/search';
	import Settings from 'lucide-svelte/icons/settings';
	import UserCheck from 'lucide-svelte/icons/user-check';
	import UserCog from 'lucide-svelte/icons/user-cog';
	import UserPlus from 'lucide-svelte/icons/user-plus';
	import UserX from 'lucide-svelte/icons/user-x';
	import Users from 'lucide-svelte/icons/users';
	import HandHeart from 'lucide-svelte/icons/hand-heart';
</script>

<main class="flex h-screen flex-row">
	<!-- sidenav -->
	<div class="flex h-full max-h-screen w-1/6 flex-grow flex-col overflow-y-auto border-r">
		<!-- header -->
		<a href="###" class="flex h-14 items-center gap-2 border-b p-4">
			<span class="font-semibold">Project PRIM</span>
		</a>
		<!-- sidenav -->
		<nav class="flex h-full flex-col justify-between">
			<div class="flex flex-col gap-2 p-2">
				<a
					href="/home"
					class="flex items-center gap-3 rounded-lg bg-muted px-3 py-2 text-primary transition-all hover:text-primary"
				>
					<Home class="h-4 w-4" />
					<p class="text-sm font-medium">Home</p>
				</a>
				<a
					href="/Patients"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<HandHeart class="h-4 w-4" />
					<p class="text-sm font-medium">Services</p>
				</a>
				<hr />
				<a
					href="/Patients"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<Users class="h-4 w-4" />
					<p class="text-sm font-medium">Patients</p>
				</a>
				<a
					href="/clearance"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<CalendarClock class="h-4 w-4" />
					<p class="text-sm font-medium">Appointments</p>
				</a>
				<a
					href="/clearance"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<Banknote class="h-4 w-4" />
					<p class="text-sm font-medium">Billing and Invoicing</p>
				</a>
				<a
					href="/clearance"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<Activity class="h-4 w-4" />
					<p class="text-sm font-medium">Reports and Analytics</p>
				</a>
			</div>
			<div class="flex flex-col gap-2 p-2">
				<a
					href="/settings"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<Settings class="h-4 w-4" />
					<p class="text-sm font-medium">System Settings</p>
				</a>
				<hr />
				<a
					href="/account"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:text-primary"
				>
					<UserCog class="h-4 w-4" />
					<p class="text-sm font-medium">Account Settings</p>
				</a>
				<a
					href="/settings"
					class="flex items-center gap-3 rounded-lg px-3 py-2 text-muted-foreground transition-all hover:bg-red-700 hover:text-white"
				>
					<Logout class="h-4 w-4" />
					<p class="text-sm font-medium">Logout</p>
				</a>
			</div>
		</nav>
	</div>

	<div class="flex h-full w-full flex-col lg:w-5/6">
		<!-- topbar -->
		<div class="flex h-14 w-full items-center justify-between border-b p-4">
			<span class="font-semibold">Home</span>
			<DropdownMenu.Root>
				<DropdownMenu.Trigger asChild let:builder>
					<Button builders={[builder]} variant="secondary" size="icon" class="rounded-full">
						<CircleUser class="h-5 w-5" />
					</Button>
				</DropdownMenu.Trigger>
				<DropdownMenu.Content align="end">
					<div class="flex flex-col p-2">
						<p class="text-sm font-bold">AccountNameHere</p>
						<p class="text-xs">AccountNumberHere</p>
						<p class="text-xs">DepartmentHere</p>
					</div>
					<DropdownMenu.Separator />
					<DropdownMenu.Item class="gap-2">
						<a href="###" class="flex w-full items-center justify-between gap-2">
							<span class="font-semibold">Logout</span>
							<Logout class="h-5 w-5 rounded-full" />
						</a>
					</DropdownMenu.Item>
				</DropdownMenu.Content>
			</DropdownMenu.Root>
		</div>

		<!-- main content -->
		<main class="flex h-auto flex-col gap-2 overflow-y-auto p-2">
			<!-- values -->
			<div class="">
				<Card.Root>
					<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-4">
						<Card.Title class="text-xl font-bold">System Analytics</Card.Title>
						<Badge variant="outline">OVERVIEW</Badge>
					</Card.Header>
					<Card.Content>
						<div class="grid gap-2 lg:grid-cols-4">
							<Card.Root>
								<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-2">
									<Card.Title class="text-sm font-medium">Patients Scheduled</Card.Title>
									<Users class="h-4 w-4 text-muted-foreground" />
								</Card.Header>
								<Card.Content>
									<div class="text-3xl font-bold">000</div>
									<p class="text-xs text-muted-foreground">--/--/----</p>
								</Card.Content>
							</Card.Root>
							<Card.Root>
								<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-2">
									<Card.Title class="text-sm font-medium">Patients Served</Card.Title>
									<UserCheck class="h-4 w-4 text-muted-foreground" />
								</Card.Header>
								<Card.Content>
									<div class="text-3xl font-bold">000</div>
									<p class="text-xs text-muted-foreground">--/--/----</p>
								</Card.Content>
							</Card.Root>
							<Card.Root>
								<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-2">
									<Card.Title class="text-sm font-medium">Patients Remaining</Card.Title>
									<UserX class="h-4 w-4 text-muted-foreground" />
								</Card.Header>
								<Card.Content>
									<div class="text-3xl font-bold">000</div>
									<p class="text-xs text-muted-foreground">--/--/----</p>
								</Card.Content>
							</Card.Root>
							<Card.Root>
								<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-2">
									<Card.Title class="text-sm font-medium">Patient in Queue</Card.Title>
									<Activity class="h-4 w-4 text-muted-foreground" />
								</Card.Header>
								<Card.Content>
									<div class="text-3xl font-bold">000</div>
									<p class="text-xs text-muted-foreground">--/--/----</p>
								</Card.Content>
							</Card.Root>
						</div>
						<div class="flex flex-wrap items-center gap-4 pt-5">
							<Button variant="outline">
								<UserPlus class="mr-2 h-4 w-4" />
								New Patient
							</Button>
							<Button variant="outline">
								<CalendarPlus class="mr-2 h-4 w-4" />
								Add to Schedule
							</Button>
							<Button variant="outline">
								<CreditCard class="mr-2 h-4 w-4" />
								Issue Card
							</Button>
							<Button variant="outline">
								<Coins class="mr-2 h-4 w-4" />
								Issue Quotation
							</Button>
							<Button variant="outline">
								<ScrollText class="mr-2 h-4 w-4" />
								Issue Medical Certificate
							</Button>
						</div>
					</Card.Content>
				</Card.Root>
			</div>

			<!-- Patient info -->
			<div class="h-full">
				<Card.Root>
					<Card.Header class="flex flex-row items-center justify-between space-y-0 pb-4">
						<Card.Title class="text-xl font-bold">Patient Information</Card.Title>
						<Badge variant="outline">LIVE UPDATES</Badge>
					</Card.Header>
					<Card.Content>
						<div class="flex h-full flex-col gap-2 lg:flex-row">
							<!-- masterlist card -->
							<Card.Root class="h-auto lg:w-4/6">
								<Tabs.Root>
									<Card.Header class="flex flex-col gap-2">
										<div class="flex flex-row">
											<Card.Title>Patient Masterlist</Card.Title>
											<div class="flex w-full flex-row place-content-end gap-2">
												<Input
													id="search"
													class="col-span-1 text-right"
													placeholder="Search here..."
												/>
												<div class="flex flex-row place-content-end gap-2">
													<Button variant="outline" size="icon">
														<Search class="h-4 w-4" />
													</Button>
												</div>
											</div>
										</div>
									</Card.Header>
									<hr />
									<!-- pagination -->
									<div class="self-end px-6 pt-6">
										<!-- pagination pc -->
										<div class="hidden flex-row justify-between lg:flex">
											<div class="">
												<Tabs.List>
													<Tabs.Trigger value="all">All</Tabs.Trigger>
													<Tabs.Trigger value="ok!">Male</Tabs.Trigger>
													<Tabs.Trigger value="inc">Female</Tabs.Trigger>
												</Tabs.List>
											</div>
											<div class="">
												<Pagination.Root count={1000} perPage={4} let:pages let:currentPage>
													<Pagination.Content>
														<Pagination.Item>
															<Pagination.PrevButton />
														</Pagination.Item>
														{#each pages as page (page.key)}
															{#if page.type === 'ellipsis'}
																<Pagination.Item>
																	<Pagination.Ellipsis />
																</Pagination.Item>
															{:else}
																<Pagination.Item isVisible={currentPage == page.value}>
																	<Pagination.Link {page} isActive={currentPage == page.value}>
																		{page.value}
																	</Pagination.Link>
																</Pagination.Item>
															{/if}
														{/each}
														<Pagination.Item>
															<Pagination.NextButton />
														</Pagination.Item>
													</Pagination.Content>
												</Pagination.Root>
											</div>
										</div>
									</div>
									<Tabs.Content value="all">
										<Card.Content class="flex h-full w-full flex-col justify-between">
											<Table.Root>
												<Table.Header>
													<Table.Row>
														<Table.Head class="xl:table.-column">Status</Table.Head>
														<Table.Head>Name</Table.Head>
														<Table.Head class="hidden sm:table-cell">Last Visit</Table.Head>
														<Table.Head class="xl:table.-column text-right"
															>Next Scheduled Visit</Table.Head
														>
													</Table.Row>
												</Table.Header>
												<!-- 4 Patients max (recent) -->
												<Table.Body>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="bg-amber-500 font-mono text-xs" variant="default"
																>OBSERVE</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">WANG MALOU</div>
															<div class="text-xs text-muted-foreground md:inline">3000187592</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="bg-emerald-600 font-mono text-xs" variant="default"
																>GOOD</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">LIM MADDIE</div>
															<div class="text-xs text-muted-foreground md:inline">3000019758</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="bg-violet-600 font-mono text-xs" variant="default"
																>RETURN</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">LEE CAO-A</div>
															<div class="text-xs text-muted-foreground md:inline">3000085140</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="font-mono text-xs" variant="destructive"
																>EMERGENCY</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">NOLA ARIA</div>
															<div class="text-xs text-muted-foreground md:inline">3000017883</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="bg-emerald-600 font-mono text-xs" variant="default"
																>GOOD</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">DANQUIT JONATHAN</div>
															<div class="text-xs text-muted-foreground md:inline">3000117298</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="bg-emerald-600 font-mono text-xs" variant="default"
																>GOOD</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">KHO MA. AZONA</div>
															<div class="text-xs text-muted-foreground md:inline">3000019778</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
													<!-- Patient 1 -->
													<Table.Row>
														<Table.Cell class="xl:table.-column">
															<Badge class="font-mono text-xs" variant="destructive"
																>EMERGENCY</Badge
															>
														</Table.Cell>
														<Table.Cell class="flex flex-col">
															<div class="font-bold">GUETTA LON</div>
															<div class="text-xs text-muted-foreground md:inline">3000018758</div>
														</Table.Cell>
														<Table.Cell class="hidden sm:table-cell">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
														<Table.Cell class="text-right">
															<div class="font-medium">----/--/-- | 00:00:00</div>
														</Table.Cell>
													</Table.Row>
												</Table.Body>
											</Table.Root>
											<hr />
										</Card.Content>
									</Tabs.Content>
								</Tabs.Root>
							</Card.Root>
							<!-- stud detail card -->
							<Card.Root class="h-auto lg:w-2/6">
								<Card.Header class="flex flex-col gap-2">
									<div class="flex w-full flex-row place-content-between items-center">
										<Card.Title>Patient Details</Card.Title>
										<div class="flex w-full flex-row place-content-end gap-2">
											<Button variant="outline" size="icon">
												<Pencil class="h-4 w-4" />
											</Button>
											<Button variant="outline" size="icon">
												<Save class="h-4 w-4" />
											</Button>
										</div>
									</div>
								</Card.Header>
								<hr />
								<Card.Content>
									<div class="flex flex-col items-center gap-4 pt-5">
										<div class="flex w-full flex-col items-start gap-2">
											<Label for="studNum" class="text-right">Patient Number</Label>
											<Input readonly class="col-span-3" placeholder="30000031859" />
										</div>
										<div class="flex flex-row gap-2">
											<div class="flex w-full flex-col items-start gap-2">
												<Label for="lastName" class="text-right">Last Name</Label>
												<Input readonly id="lastName" class="col-span-3" placeholder="Dela Cruz" />
											</div>
											<div class="flex w-full flex-col items-start gap-2">
												<Label for="firstName" class="text-right">First Name</Label>
												<Input readonly id="firstName" class="col-span-3" placeholder="Juan" />
											</div>
										</div>
									</div>
								</Card.Content>
								<hr />
								<Card.Content>
									<div class="flex w-full flex-col items-start gap-2 pt-6">
										<div class="flex flex-row">
											<div class="flex flex-col gap-1">
												<Label>Patient Status</Label>
											</div>
											<div class="flex w-full flex-row flex-wrap justify-end gap-1">
												<Badge class="font-mono text-xs" variant="outline">GOOD</Badge>
												<Badge class="font-mono text-xs" variant="outline">OBSERVE</Badge>
												<Badge class="font-mono text-xs" variant="outline">RETURN</Badge>
												<Badge class="font-mono text-xs" variant="outline">EMERGENCY</Badge>
											</div>
										</div>
										<div class="flex w-full flex-col items-start gap-2">
											<div class="flex w-full flex-col">
												<Label for="firstName">Recent Vital Signs</Label>
												<Label class="text-xs">as of $dateHere</Label>
											</div>
											<Textarea
												readonly
												id="firstName"
												class="col-span-3"
												placeholder="Recent vitals here"
											/>
										</div>
										<div class="flex w-full flex-col items-start gap-2">
											<div class="flex w-full flex-col">
												<Label for="firstName">Recent Remarks</Label>
												<Label class="text-xs">as of $dateHere</Label>
											</div>
											<Textarea
												readonly
												id="firstName"
												class="col-span-3"
												placeholder="Recent vitals here"
											/>
										</div>
										<div class="flex w-full flex-col items-start gap-2">
											<div class="flex w-full flex-col">
												<Label for="firstName">Recent Diagnosis</Label>
												<Label class="text-xs">as of $dateHere</Label>
											</div>
											<Textarea
												readonly
												id="firstName"
												class="col-span-3"
												placeholder="Recent vitals here"
											/>
										</div>
									</div>
								</Card.Content>
							</Card.Root>
						</div>
					</Card.Content>
				</Card.Root>
			</div>
		</main>
	</div>
</main>
