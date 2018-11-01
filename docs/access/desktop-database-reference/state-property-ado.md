---
title: Свойство State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8ea3738465ed9bfc10cbabdf355036f7c160f66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886615"
---
# <a name="state-property-ado"></a>Свойство State (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.

Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением. Значение по умолчанию — **adStateClosed**.

## <a name="remarks"></a>Замечания

Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.

Свойство **состояние** объекта может содержать комбинацию значений. Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.

Свойство **State** доступен только для чтения.

