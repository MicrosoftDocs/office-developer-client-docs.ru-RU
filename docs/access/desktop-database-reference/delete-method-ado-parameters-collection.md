---
title: Метод удаления (коллекция параметров ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294094"
---
# <a name="delete-method-ado-parameters-collection"></a>Метод удаления (коллекция параметров ADO)

**Область применения**: Access 2013, Office 2013

Удаляет объект из коллекции [Параметры.](parameters-collection-ado.md)

## <a name="syntax"></a>Синтаксис

*Параметры*. Удаление *индекса*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Index* |Значение **String,** содержаное имя объекта, который необходимо удалить, или координатную позицию (индекс) объектов в коллекции.|

## <a name="remarks"></a>Примечания

Использование метода **Delete** в коллекции позволяет удалить один из объектов в коллекции. Этот метод доступен только в коллекции **Параметры** объекта [Command.](command-object-ado.md) При вызове метода **Delete** необходимо использовать свойство Имя объекта [Параметр](parameter-object-ado.md) или его индекс коллекции — переменная объекта не является допустимым аргументом. [](name-property-ado.md)

