---
title: Recordset2.UpdateOptions Property (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 508727437506e418fa2c8804cc9974f6d3ee7691
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480631"
---
# <a name="recordset2updateoptions-property-dao"></a>Recordset2.UpdateOptions Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . UpdateOptions

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

При выполнении пакетного режима **[обновления](recordset2-update-method-dao.md)** DAO и текущей позиции пакета клиентской библиотеки создать ряд инструкций SQL UPDATE, внесите необходимые изменения. Для каждого обновления для изоляции записей, которые помечены как измененный свойством **[RecordStatus](recordset2-recordstatus-property-dao.md)** создается инструкцию SQL. Так как некоторые удаленных серверов с помощью триггеров или другие способы целостность данных, он часто необходимо ограничить поля обновляется только теми, которые повлияет переход. 

Чтобы сделать это, присвойте свойству **UpdateOptions** к одной из констант **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**или **dbCriteriaTimeStamp**. Таким образом, выполняется только абсолютный минимальный объем кода триггер. В результате операции обновления выполняется быстрее и с меньшим количеством возможных ошибок.

Также можно объединять константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate** , чтобы определить, следует ли использовать набор SQL DELETE и инструкций INSERT или инструкции SQL UPDATE для каждого обновления при отправке пакетные изменения на сервере. В первом случае две отдельные операции требуются для обновления записи. В некоторых случаях особенно где удаленная система implements удаления, вставки и обновления триггеров, выбрав правильное значение свойства **UpdateOptions** можно значительно повысить производительность.

Если не указать любой константы, будет использоваться **dbCriteriaUpdate** и **dbCriteriaKey** .

Недавно добавленных записей всегда будет выдавать инструкции INSERT и удаленных записей всегда будет выдавать инструкций DELETE, поэтому это свойство применяется только к как библиотека курсора обновляет измененные записи.
