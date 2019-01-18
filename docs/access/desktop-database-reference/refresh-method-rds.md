---
title: Метод Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718723"
---
# <a name="refresh-method-rds"></a>Метод Refresh (RDS)

**Применимо к**: Access 2013, Office 2013

Повторный запрос источника данных, указанных в свойстве [подключение](connect-property-rds.md) и обновляет результаты запроса.

## <a name="syntax"></a>Синтаксис

*DataControl*. Обновление

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|

## <a name="remarks"></a>Замечания

Прежде чем использовать метод **Refresh** , необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) . Все элементы управления с привязкой к данным на форму, связанную с **RDS. DataControl** объекта будет содержать новый набор записей. Выпущен любого существующего объекта [набора записей](recordset-object-ado.md) и не учитываются несохраненные изменения. Метод **Refresh** автоматически преобразует первую запись текущей записи.

Рекомендуется вызвать метод **Refresh** периодически при работе с данными. Если извлечения данных и оставьте его на клиентском компьютере какое-то время, скорее всего, устаревший. Существует возможность, что все изменения, внесенные завершится с ошибкой, так как другому пользователю, могут измениться эту запись и отправил изменения перед выполнением.

