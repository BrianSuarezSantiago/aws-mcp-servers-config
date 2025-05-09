# Amazon Q Developer CLI

1. Instalar Amazon Q Developer CLI: https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html | https://github.com/aws/amazon-q-developer-cli
2. Configurar Amazon Q Developer CLI
3. Instalar uv desde Astral: https://docs.astral.sh/uv/getting-started/installation/
4. Instalar una version de Python 3.10 o superior: `uv python install 3.10` (o una versión más reciente)

No he conseguido que funcione con Docker

5. Crear un archivo `mcp.json`
     Global Configuration: `~/.aws/amazonq/mcp.json` - Aplica a todos los workspaces

     Workspace Configuration: `.amazonq/mcp.json` - Aplica especificamente al workspace actual

     MCP Configuration: https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-mcp-configuration.html

     AWS MCP Servers: https://awslabs.github.io/mcp/ | https://github.com/awslabs/mcp
7. Incluir la configuración del servidor

Usando `uv`

```{json}
{
  "mcpServers": {
    "aws-docs": {
        "command": "uvx",
        "args": ["awslabs.aws-documentation-mcp-server@latest"],
        "env": {
          "FASTMCP_LOG_LEVEL": "ERROR"
        },
        "disabled": false,
        "autoApprove": []
    }
  }
}
```

## Comandos Amazon Q Developer CLI

`/tools` para ver las tools configurados

`/tools trust <tools>` para usar las tools sin tener que pedir las confirmacion constantemente

## Prompts Examples

look up documentation on S3 bucket naming rule. cite your sources --> recommend content for page https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html
