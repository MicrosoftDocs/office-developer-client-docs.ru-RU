---
title: '14 главы: Базовые концепции ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8079851a59e8fe0d077dcbeed5b354e924aca6a2
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936736"
---
# <a name="chapter-14-ado-md-fundamentals"></a>14 главы: Базовые концепции ADO MD

**Применимо к**: Access 2013, Office 2013

Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++. ADO MD расширяет возможности Microsoft ActiveX Data Objects (ADO) для включения объектов, относящихся к многомерных данных, таких как объекты [CubeDef](cubedef-object-ado-md.md) и [ячеек](cellset-object-ado-md.md) . С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.

Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным. Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP. MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений. Обратитесь к документации для поставщика OLE DB для OLAP более подробные сведения о конкретных синтаксис и поведение поддерживается поставщиком.

В этом документе предполагается знание языка программирования Visual Basic и общие знания ADO и OLAP. Для получения дополнительных сведений см. [Руководство программиста ADO](ado-programmer-s-guide.md) и OLE DB для OLAP программиста ссылку. 

В этой главе рассматриваются следующие темы:

- [Общие сведения о многомерных схемы и данных](overview-of-multidimensional-schemas-and-data.md)
- [Работа с многомерных данных](working-with-multidimensional-data.md)
- [Использование ADO с ADO MD](using-ado-with-ado-md.md)
- [Программирование с помощью ADO MD](programming-with-ado-md.md)
