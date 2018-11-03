---
title: Удаление метода (коллекции полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afeec4007b9bd44a9575217e1fb6380a50d699c3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945318"
---
# <a name="delete-method-ado-fields-collection"></a>Удаление метода (коллекции полей ADO)


**Применимо к**: Access 2013, Office 2013



Удаляет объект из коллекции [полей](fields-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Поля*. Удаление*поля*

## <a name="parameters"></a>Параметры

- *Поле*

  - **Variant** , который определяет удаляемый объект [поля](field-object-ado.md) . Этот параметр может быть имя объекта **поля** или порядковый номер самого объекта **поля** .

## <a name="remarks"></a>Примечания

Вызов метода **Fields.Delete** для открытия [набора записей](recordset-object-ado.md) вызывает ошибку времени выполнения.

