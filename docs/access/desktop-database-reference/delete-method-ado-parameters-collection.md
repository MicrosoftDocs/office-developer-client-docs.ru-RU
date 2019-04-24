---
title: Метод Delete (Коллекция параметров ADO)
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
# <a name="delete-method-ado-parameters-collection"></a>Метод Delete (Коллекция параметров ADO)

**Область применения**: Access 2013, Office 2013

Удаляет объект из коллекции [Parameters](parameters-collection-ado.md) .

## <a name="syntax"></a>Синтаксис

*Параметры*. Удаление *индекса*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Index* |**Строковое** значение, содержащее имя удаляемого объекта или порядковый номер объекта (индекса) в коллекции.|

## <a name="remarks"></a>Замечания

Использование метода **Delete** для коллекции позволяет удалить один из объектов в коллекции. Этот метод доступен только для коллекции **Parameters** объекта [Command](command-object-ado.md) . При вызове метода **Delete** необходимо использовать свойство [Name](name-property-ado.md) объекта [Parameter](parameter-object-ado.md) или его индекс (объектная переменная не является допустимым аргументом).

