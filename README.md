# Selección de un ERP: matriz de decisión para dos empresas

**Sistemas de Gestión Empresarial (SGE)**
2º DAW, UT1 - Actividad evaluable 01.
Desarrollado por **Daniel Dimitrov** y **Melisa Vafaeva**.

## Visión general

- **Objetivo:** recomendar un ERP a dos empresas comparando **Odoo Enterprise**, **Holded** y **Microsoft Dynamics 365 Business Central**.
- **Empresa 1, Supermercado La Plaza:** 5 personas, una tienda, 2.500 referencias y 650.000 € de facturación, con presupuesto tecnológico muy limitado.
- **Empresa 2, Reformas Levante:** 45 empleados, 6 M€ de facturación y entre 15 y 20 obras simultáneas en Valencia y Castellón.
- **Método:** matriz de decisión con seis criterios ponderados, valoración de 0 a 3 y puntuación `(valoración x peso) / 3`, con nota final sobre 100.
- **Herramienta:** matriz web en HTML y JavaScript, con pesos, valoraciones e importes de TCO editables.

## Resultados

| Puntuación sobre 100 | Odoo Enterprise | Holded | MS Dynamics 365 Business Central |
|:-|:-:|:-:|:-:|
| Supermercado La Plaza | **85,00** | 81,67 | 45,00 |
| Reformas Levante | **88,33** | 68,33 | 75,00 |

**Recomendación:** Odoo Enterprise en los dos casos. Para el supermercado, Holded es el plan B si no se puede asumir la implantación. Para la empresa de reformas, Business Central es la alternativa más sólida, aunque sale más cara a 5 años.

## Mapa de documentación

- [Informe de entrega](Documentacion/informe.md): matrices, conclusiones y comentarios sobre el uso de la IA.
- [Justificación detallada](Documentacion/justificacion.md): justificación de cada puntuación, cálculo del TCO a 5 años y nota sobre Verifactu.
- [Matriz de decisión](matriz/index.html): página interactiva.
- Capturas de la matriz:
  - [Empresa 1: Supermercado La Plaza](capturas/matriz_empresa1_supermercado.png)
  - [Empresa 2: Reformas Levante](capturas/matriz_empresa2_reformas.png)

## Uso de la matriz

Abrir `matriz/index.html` en el navegador; no necesita servidor ni instalación. Desde la página se pueden cambiar pesos, valoraciones e importes de TCO, y todo se recalcula al momento. El botón **Restablecer valores del informe** devuelve los datos entregados.

Para comprobar los cálculos con Node.js desde la raíz del proyecto:

```
node matriz/verificar.js
```

El script valida los pesos, la escala, las justificaciones, las fuentes, los totales y los TCO, y termina con `Todo correcto.` si todo coincide con el informe.
