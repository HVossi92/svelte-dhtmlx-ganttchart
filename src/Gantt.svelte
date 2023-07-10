<script>
    import "./lib/trial-gantt/codebase/dhtmlxgantt.css";
    import { onMount } from "svelte";
    import { Gantt } from "@dhx/trial-gantt";
    
  const tasks = {
    data: [
      {
        id: "10",
        text: "Project #1",
        start_date: "01-04-2025",
        duration: 3,
        order: 10,
        progress: 0.4,
        open: true,
      },
      {
        id: "1",
        text: "Task #1",
        start_date: "01-04-2025",
        duration: 1,
        order: 10,
        progress: 0.6,
        parent: "10",
      },
      {
        id: "2",
        text: "Task #2",
        start_date: "02-04-2025",
        duration: 2,
        order: 20,
        progress: 0.6,
        parent: "10",
      },
    ],
    links: [{ id: 1, source: 1, target: 2, type: "0" }],
  };

    
    let container;
    onMount(() => {
        let gantt = Gantt.getGanttInstance();
        gantt.init(container);
        gantt.parse(tasks);

        return () => {
            gantt.destructor();
        };
    });
</script>

<div bind:this={container} style="width: 100%; height: 100%;"></div>