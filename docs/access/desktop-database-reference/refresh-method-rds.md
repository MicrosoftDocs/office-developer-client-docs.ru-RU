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

Повторно запрашивает источник данных, указанный в свойстве [Connect,](connect-property-rds.md) и обновляет результаты запроса.

## <a name="syntax"></a>Синтаксис

*DataControl*. Обновление

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|

## <a name="remarks"></a>Заметки

Перед использованием метода [Refresh](connect-property-rds.md) [необходимо](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) SQL свойства Connect, [Server](server-property-rds.md)и **SQL.** Все связанные с данными элементы управления в форме, связанные с **RDS. Объект DataControl** отражает новый набор записей. Все существующие [объекты Recordset](recordset-object-ado.md) отпущены, а все несъемные изменения удаляются. Метод **Refresh** автоматически делает первую запись текущей.

При работе с данными стоит периодически вызывать метод **Refresh.** Если вы извлекаете данные, а затем оставляете их на клиентской машине на некоторое время, скорее всего, они будут устарели. Возможно, что любые внесенные изменения не удастся, так как кто-то другой мог изменить запись и внести изменения до вас.

