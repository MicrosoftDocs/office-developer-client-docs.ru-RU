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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309301"
---
# <a name="refresh-method-rds"></a>Метод Refresh (RDS)

**Область применения**: Access 2013, Office 2013

Повторно запрашивает источник данных, указанный в свойстве [Connect](connect-property-rds.md) , и обновляет результаты запроса.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. Обновление

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|

## <a name="remarks"></a>Замечания

Прежде чем использовать метод **Refresh** , необходимо задать свойства [Connect](connect-property-rds.md), [Server](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) . Все элементы управления с привязкой к данным в форме, связанной с **RDS. Объект элемента управления** данным будет отражать новый набор записей. Освобождается любой существующий объект [Recordset](recordset-object-ado.md) , а все несохраненные изменения отбрасываются. Метод **Refresh** автоматически создает первую запись в текущей записи.

Рекомендуется периодически вызывать метод **Refresh** при работе с данными. Если получить данные, а затем оставить их на клиентском компьютере в течение этого времени, скорее всего, оно станет устаревшим. Возможно, все внесенные изменения не будут выполнены, так как другой пользователь изменил запись и отправил изменения.

