<script>
  const services = [
    {
      leftIcon: "/images/Website logo.png",
      title: "Website Development",
      desc: "Reliable, fast and safe. Modern best practice.",
    },
    {
      rightIcon: "/images/Python.png",
      title: "Backend Programming",
      desc: "Reliable, fast and safe. Modern best practice.",
    },
    {
      leftIcon: "/images/Flutter.png",
      title: "Custom Apps",
      desc: "We design and build bespoke Android / iOS apps.",
    },
    {
      rightIcon: "/images/API logo.png",
      title: "API Integration",
      desc: "Connect your systems and services seamlessly with API solutions",
    },
    {
      leftIcon: "/images/Webhooks logo.png",
      title: "Webhooks",
      desc: "Realtime event handling and automation with webhooks.",
    },
    {
      rightIcon: "/images/Cloud hosting.png",
      title: "Cloud Hosting",
      desc: "Scaling, Deployment, Infrastructure, Docker or VM, Kubernetes, Azure, GCP",
    },
    {
      leftIcon: "/images/Device logo.png",
      title: "Device Configuration",
      desc: "Wifi, Access Point, Router, Wifi-Extender, Networks, Computers, Android Phones",
    },
    {
      rightIcon: "/images/Database logo.png",
      title: "Database",
      desc: "MySQL, PostgreSQL, MariaDB Administration, Queries, Table Design, SCHEMA changes",
    },
    {
      leftIcon: "/images/Backups logo.png",
      title: "Backups",
      desc: "Setup, Schedules, Integrity Check, Recomendations",
    },
    {
      rightIcon: "/images/Server logo.png",
      title: "Server Administration",
      desc: "Linux or MacOS, SSH, bash scripting, updates, upgrades, software setup such as webserver, application server",
    },
  ];
</script>


<h1>Our Services</h1>
<ul>
  <li>Web Development</li>
  <li>Mobile App Development</li>
  <li>UI/UX Design</li>
</ul>

<main>
  
	<div class="services-container">
		{#each Array(5) as _, i}
			<div class="row">
				<!-- Left Column -->
				<div class="col left">
					<div class="content-wrapper">
						{#if services[i * 2].leftIcon}
							<img src={services[i * 2].leftIcon} alt={services[i * 2].title} class="icon-img" />
						{:else}
							<!-- Placeholder for custom SVGs/Icons if you want to rebuild those -->
							<div class="icon-placeholder"></div>
						{/if}
						<div class="text">
							<h3>{services[i * 2].title}</h3>
							<p>{services[i * 2].desc}</p>
						</div>
					</div>
				</div>

				<!-- Right Column -->
				<div class="col right">
					<div class="content-wrapper">
						<div class="text">
							<h3>{services[i * 2 + 1].title}</h3>
							<p>{services[i * 2 + 1].desc}</p>
						</div>
						<img
							src={services[i * 2 + 1].rightIcon}
							alt={services[i * 2 + 1].title}
							class="icon-img"
						/>
					</div>
				</div>
			</div>
		{/each}
	</div>
</main>

<style>
  
	/* Services Grid */
	.services-container {
		width: 100%;
		border-bottom: 1.5px solid #444;
	}
	.row {
		display: flex;
		width: 100%;
		border-bottom: 1.5px solid #444;
	}
	.row:last-child {
		border-bottom: none;
	}

	.col {
		flex: 1;
		padding: 20px;
		display: flex;
		align-items: center;
		box-sizing: border-box;
	}
	.col.left {
		border-right: 1.5px solid #444;
	}

	.content-wrapper {
		display: flex;
		align-items: center;
		gap: 20px;
		width: 100%;
	}

	.col.left .content-wrapper {
		justify-content: flex-start;
	}
	.col.right .content-wrapper {
		justify-content: flex-end;
		text-align: right;
	}

	.text h3 {
		margin: 0 0 8px 0;
		font-size: 1.1rem;
		color: #333;
	}
	.text p {
		margin: 0;
		font-size: 0.9rem;
		line-height: 1.4;
		color: #666;
	}

	.icon-img {
		height: 80px; /* Adjust size to match flyer */
		width: auto;
		flex-shrink: 0;
	}

	.icon-placeholder {
		width: 80px;
		height: 80px;
		background: #ddd; /* Example placeholder */
		flex-shrink: 0;
	}
	/* Mobile Responsiveness */
	@media (max-width: 768px) {
		.row {
			flex-direction: column;
		}
		.col.left {
			border-right: none;
			border-bottom: 1.5px solid #444;
		}
		.col.right .content-wrapper {
			justify-content: flex-start;
			text-align: left;
			flex-direction: row-reverse;
		}
		.icon-img {
			height: 60px;
		}
	}
</style>