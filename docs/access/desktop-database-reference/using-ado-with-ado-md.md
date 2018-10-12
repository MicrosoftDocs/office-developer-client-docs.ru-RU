---
title: Using ADO with ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492efdcef5f71daf50ac84eec5e61ef4ed07fd5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481625"
---
# <a name="using-ado-with-ado-md"></a>Using ADO with ADO MD


**Применимо к**: Access 2013 | Office 2013

ADO и ADO MD, связанных с ними, но отдельные объектных моделей. ADO предоставляет объекты для подключения к источникам данных, выполнение команд, получение табличных данных и метаданных схемы в табличном формате и просмотра сведений об ошибках поставщика. ADO MD предоставляет объекты для извлечения многомерных данных и Просмотр многомерных схемы метаданных.

При работе с MDP можно использовать ADO, ADO MD или оба вместе с приложением. С учетом обе библиотеки в проекте, будут иметь полный доступ к функциональные возможности, предоставляемые вашей MDP.

Часто бывает полезно для потребителей для получения плоская, табличного представления многомерного набора данных. Это можно сделать с помощью объекта ADO [набора записей](recordset-object-ado.md) . Укажите источник для вашей [ячеек](cellset-object-ado-md.md) в качестве ***источника*** параметра для метода [Open](open-method-ado-recordset.md) **набора записей**, а не как источник ADO MD **ячеек**.

Также можно использовать для просмотра метаданных схемы в табличном представлении, а не как иерархия объектов. Метод ADO [OpenSchema](openschema-method-ado.md) на объект [подключения](connection-object-ado.md) позволяет пользователю открывать **набора записей** , содержащий сведения о схеме. Параметр ***QueryType*** метода **OpenSchema** имеет несколько значений [SchemaEnum](schemaenum.md) , связанных с MDPs. Доступны следующие значения:

  - **adSchemaCubes**

  - **adSchemaDimensions**

  - **adSchemaHierarchies**

  - **adSchemaLevels**

  - **adSchemaMeasures**

  - **adSchemaMembers**

Чтобы использовать значения перечислений ADO с ADO MD свойствам и методам, проект должен содержать ссылки ADO и ADO MD библиотек. Например можно использовать значения перечисления **adState** ADO со свойством ADO MD [состояние](state-property-ado-md.md) . Дополнительные сведения о создании ссылки на библиотеки обратитесь к документации вашего средство разработки.

Дополнительные сведения о ADO объекты и методы содержатся в разделе [Справочник по API ADO](ado-api-reference.md).
