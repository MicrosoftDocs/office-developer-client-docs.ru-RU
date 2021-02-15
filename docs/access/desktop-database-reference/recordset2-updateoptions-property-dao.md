---
title: Свойство Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309105"
---
# <a name="recordset2updateoptions-property-dao"></a>Свойство Recordset2.UpdateOptions (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* UpdateOptions

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

При выполнении **[](recordset2-update-method-dao.md)** обновления в пакетном режиме DAO и клиентская пакетная библиотека курсоров создают серию SQL update, чтобы внести необходимые изменения. Для SQL создается предложение WHERE для каждого обновления, чтобы изолировать записи, помеченные как измененные **[свойством RecordStatus.](recordset2-recordstatus-property-dao.md)** Так как некоторые удаленные серверы используют триггеры или другие способы обеспечения целостности данных, часто важно ограничить поля, обновляемые только теми, на которые влияет изменение. 

Для этого установите для свойства **UpdateOptions** одну из констант **dbCriteriaKey,** **dbCriteriaModValues,** **dbCriteriaAllCols** или **dbCriteriaTimeStamp.** Таким образом выполняется только абсолютный минимальный объем кода триггера. В результате операция обновления выполняется быстрее и с меньшем количеством потенциальных ошибок.

Вы также можете совмедить константы **dbCriteriaDeleteInsert** или **dbCriteriaUpdate,** чтобы определить, следует ли использовать набор SQL DELETE и INSERT или SQL UPDATE для каждого обновления при отправке пакетных изменений обратно на сервер. В этом случае для обновления записи требуются две отдельные операции. В некоторых случаях, особенно если удаленная система реализует триггеры DELETE, INSERT и UPDATE, выбор правильного параметра **свойства UpdateOptions** может значительно повлиять на производительность.

Если не указать константы, будут использоваться **dbCriteriaUpdate** и **dbCriteriaKey.**

Добавленные записи всегда будут создавать записи INSERT, а удаленные записи всегда будут создавать заявления DELETE, поэтому это свойство применяется только к обновлению измененных записей библиотекой курсоров.

