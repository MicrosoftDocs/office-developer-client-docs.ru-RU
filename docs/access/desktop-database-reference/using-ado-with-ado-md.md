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

ADO и ADO MD — это связанные, но отдельные объектные модели. ADO предоставляет объекты для подключения к источникам данных, выполнения команд, получения табулярных данных и метаданных схемы в табулярном формате, а также сведений об ошибках поставщика просмотра. ADO MD предоставляет объекты для сбора многомерных данных и просмотра многомерных метаданных схемы.

При работе с MDP вы можете использовать ADO, ADO MD или оба приложения. Ссылаясь на обе библиотеки в рамках проекта, вы будете иметь полный доступ к функциям, предоставляемым MDP.

Для потребителей часто полезно получить уплощенное табулярное представление многомерного набора данных. Это можно сделать с помощью объекта ADO [Recordset.](recordset-object-ado.md) Укажите источник для [ячейки в](cellset-object-ado-md.md) качестве параметра ***Source*** для метода [Open](open-method-ado-recordset.md) в **наборе** записей, а не как источник для ячейки ADO **MD.**

Кроме того, может быть полезно просмотреть метаданные схемы в виде табулярного представления, а не как иерархию объектов. Метод ADO [OpenSchema](openschema-method-ado.md) на [объекте Подключение](connection-object-ado.md) позволяет пользователю открыть **набор записей,** содержащий сведения о схеме. Параметр ***QueryType*** метода **OpenSchema** имеет несколько значений [SchemaEnum,](schemaenum.md) которые связаны конкретно с MDP. Эти значения:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Чтобы использовать значения ADO с свойствами или методами ADO MD, проект должен ссылаться на библиотеки ADO и ADO MD. Например, можно использовать значения ADO **adState** с свойством состояния ADO [MD.](state-property-ado-md.md) Дополнительные сведения о создании ссылок на библиотеки см. в документации средства разработки.

Дополнительные сведения об объектах и методах ADO см. в справке [ADO API.](ado-api-reference.md)

