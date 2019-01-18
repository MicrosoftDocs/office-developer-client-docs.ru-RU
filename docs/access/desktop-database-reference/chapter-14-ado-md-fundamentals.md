---
title: Глава 14. Основы ADO MD
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701139"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Глава 14. Основы ADO MD

**Применимо к**: Access 2013, Office 2013

Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++. ADO MD расширяет возможности Microsoft ActiveX Data Objects (ADO) для включения объектов, относящихся к многомерных данных, таких как объекты [CubeDef](cubedef-object-ado-md.md) и [ячеек](cellset-object-ado-md.md) . С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.

Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным. Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP. MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений. Обратитесь к документации для поставщика OLE DB для OLAP более подробные сведения о конкретных синтаксис и поведение поддерживается поставщиком.

В этом документе предполагается знание языка программирования Visual Basic и общие знания ADO и OLAP. Для получения дополнительных сведений см. [Руководство программиста ADO](ado-programmer-s-guide.md) и OLE DB для OLAP программиста ссылку. 

В этой главе рассматриваются следующие темы:

- [Обзор многомерных схем и данных](overview-of-multidimensional-schemas-and-data.md)
- [Работа с многомерными данными](working-with-multidimensional-data.md)
- [Использование ADO с ADO MD](using-ado-with-ado-md.md)
- [Программирование с помощью ADO MD](programming-with-ado-md.md)
