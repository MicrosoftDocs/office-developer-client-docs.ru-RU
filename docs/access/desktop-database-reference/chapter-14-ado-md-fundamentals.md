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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296467"
---
# <a name="chapter-14-ado-md-fundamentals"></a>Глава 14. Основы ADO MD

**Область применения**: Access 2013, Office 2013

Объекты данных Microsoft ActiveX (многомерные) (ADO MD) обеспечивают простой доступ к многомерным данным из таких языков, как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J++. ADO MD расширяет возможности ADO Data Objects (ADO) для включения объектов, относящихся к многомерным данным, таких как объекты [CubeDef](cubedef-object-ado-md.md) и набор [ячеек](cellset-object-ado-md.md) . С помощью ADO MD можно просматривать многомерные схемы, запрашивать кубы и получать результаты.

Как и ADO, ADO MD используют основного поставщика OLE DB для получения доступа к данным. Для работы с ADO MD должен использоваться поставщик многомерных данных (MDP), как определено в OLE DB для спецификации OLAP. Поставщики MDP отображают данные в многомерных представлениях в отличие от поставщиков табличных данных (TDP), отображающих данные в табличных представлениях. Дополнительные сведения о конкретном синтаксисе и поддерживаемых поставщиком действиях см. в документации для своего поставщика OLAP OLE DB.

В этом документе предполагается работа со сведениями о языке программирования Visual Basic и общие сведения об ADO и OLAP. Для получения дополнительных сведений ознакомьтесь с [руководством программиста по ADO](ado-programmer-s-guide.md) и справочником по программированию для программиста для куба OLE. 

В этой главе рассматриваются следующие темы:

- [Обзор многомерных схем и данных](overview-of-multidimensional-schemas-and-data.md)
- [Работа с многомерными данными](working-with-multidimensional-data.md)
- [Using ADO with ADO MD](using-ado-with-ado-md.md)
- [Programming with ADO MD](programming-with-ado-md.md)
