---
title: Использование ADO с ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 80c87f57a96f98de704e3cfa9b7689a522e4a7af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312749"
---
# <a name="using-ado-with-ado-md"></a>Использование ADO с ADO MD


**Область применения**: Access 2013, Office 2013

ADO и ADO MD — это связанные, но отдельные объектные модели. ADO предоставляет объекты для подключения к источникам данных, выполнения команд, получения табличные данные и метаданных схемы в табличные форматы и просмотра сведений об ошибках поставщика. ADO MD предоставляет объекты для инициации многомерных данных и просмотра метаданных многомерной схемы.

При работе с MDP вы можете использовать ADO, ADO MD или оба приложения. Ссылаясь на обе библиотеки проекта, вы сможете получить полный доступ к функциям, предоставляемым MDP.

Пользователям часто полезно получить плоское табличные представления многомерного наборов данных. Это можно сделать с помощью объекта ADO [Recordset.](recordset-object-ado.md) Укажите источник ячейки [в](cellset-object-ado-md.md) качестве параметра ***Source*** для метода [Open](open-method-ado-recordset.md) в **наборе** записей, а не в качестве источника для ячейки ADO **MD.**

Также может быть полезно просматривать метаданные схемы в таблическом представлении, а не в виде иерархии объектов. Метод ADO [OpenSchema](openschema-method-ado.md) объекта [Connection](connection-object-ado.md) позволяет пользователю открыть набор **записей,** содержащий сведения о схеме. Параметр ***QueryType*** метода **OpenSchema** имеет несколько значений [SchemaEnum,](schemaenum.md) которые относятся к MDP. Эти значения:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Чтобы использовать значения из enum ADO со свойствами или методами ADO MD, проект должен ссылаться на библиотеки ADO и ADO MD. Например, можно использовать значения из enum ADO **adState** со свойством ADO MD [State.](state-property-ado-md.md) Дополнительные сведения о создании ссылок на библиотеки см. в документации средства разработки.

Дополнительные сведения об объектах и методах ADO см. в справочнике [по ADO API.](ado-api-reference.md)

