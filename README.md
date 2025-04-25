# alibaba-cloud-ops-mcp-server

A dynamic MCP server management service that creates, runs, and manages Model Context Protocol (MCP) servers dynamically. This service itself functions as an MCP server and launches/manages other MCP servers as child processes, enabling a flexible MCP ecosystem.

<a href="https://glama.ai/mcp/servers/@aliyun/alibabacloud-core-mcp-server">
  <img width="380" height="200" src="https://glama.ai/mcp/servers/@aliyun/alibabacloud-core-mcp-server/badge" alt="AlibabaCloud Server MCP server" />
</a>

## Prepare

Install [uv](https://github.com/astral-sh/uv)

```bash
# On macOS and Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Configuration

Use [VS Code](https://code.visualstudio.com/) + [Cline](https://cline.bot/) to config MCP Server.

To use `alibaba-cloud-ops-mcp-server` MCP Server with any other MCP Client, you can manually add this configuration and restart for changes to take effect:

```json
{
  "mcpServers": {
    "alibaba-cloud-ops-mcp-server": {
      "command": "uvx",
      "args": [
        "alibaba-cloud-ops-mcp-server@latest"
      ],
      "env": {
        "ALIBABA_CLOUD_ACCESS_KEY_ID": "Your Access Key ID",
        "ALIBABA_CLOUD_ACCESS_KEY_SECRET": "Your Access Key SECRET"
      }
    }
  }
}
```

## Tools

| **Product** | **Tool** | **Function** | **Implematation** | **Status** |
| --- | --- | --- | --- | --- |
| ECS | RunCommand | Run Command | OOS | Done |
| | StartInstances | Start Instances | OOS | Done |
| | StopInstances | Stop Instances | OOS | Done |
| | RebootInstances | Reboot Instances | OOS | Done |
| | DescribeInstances | View Instances | API | Done |
| | DescribeRegions | View Regions | API | Done |
| | DescribeZones | View Zones | API | Done |
| | DescribeAvailableResource | View Resource Inventory | API | Done |
| | DescribeImages | View Images | API | Done |
| | DescribeSecurityGroups | View Security Groups | API | Done |
| | RunInstances | Create Instances | OOS | Done |
| | DeleteInstances | Delete Instances | API | Done |
| | ResetPassword | Modify Password | OOS | Done |
| | ReplaceSystemDisk | Replace Operating System | OOS | Done |
| VPC | DescribeVpcs | View VPCs | API | Done |
| | DescribeVSwitches | View VSwitches | API | Done |
| CloudMonitor | GetCpuUsageData | Get CPU Usage Data for ECS Instances | API | Done |
| | GetCpuLoadavgData | Get CPU One-Minute Average Load Metric Data | API | Done |
| | GetCpuloadavg5mData | Get CPU Five-Minute Average Load Metric Data | API | Done |
| | GetCpuloadavg15mData | Get CPU Fifteen-Minute Average Load Metric Data | API | Done |
| | GetMemUsedData | Get Memory Usage Metric Data | API | Done |
| | GetMemUsageData | Get Memory Utilization Metric Data | API | Done |
| | GetDiskUsageData | Get Disk Utilization Metric Data | API | Done |
| | GetDiskTotalData | Get Total Disk Partition Capacity Metric Data | API | Done |
| | GetDiskUsedData | Get Disk Partition Usage Metric Data | API | Done |