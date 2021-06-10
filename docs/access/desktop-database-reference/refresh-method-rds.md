---
title: Метод обновления (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309301"
---
# <a name="refresh-method-rds"></a>Метод обновления (RDS)

**Область применения**: Access 2013, Office 2013

Requeries the data source specified in the [Подключение](connect-property-rds.md) and updates the query results.

## <a name="syntax"></a>Синтаксис

*DataControl*. Обновление

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|

## <a name="remarks"></a>Примечания

Необходимо установить свойства [Подключение,](connect-property-rds.md) [server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) перед использованием метода **Обновления.** Все элементы управления, связанные с данными, в форме, связанной с **RDS. Объект DataControl** будет отражать новый набор записей. Все существующие [объекты Recordset](recordset-object-ado.md) освобождены, а все незавершенные изменения удаляются. Метод **Обновления** автоматически делает первую запись текущей записи.

При работе с данными можно периодически вызывать метод **Обновления.** Если вы извлекаете данные, а затем оставьте их на клиентской машине на некоторое время, это, скорее всего, устарело. Не исключено, что любые внесенные изменения не удастся, так как кто-то другой мог изменить запись и представить изменения перед вами.

