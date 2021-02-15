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
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308535"
---
# <a name="state-property-ado"></a>Свойство State (ADO)


**Область применения**: Access 2013, Office 2013

Указывает на все применимые объекты, независимо от того, является ли состояние объекта открытым или закрытым.

Указывает для всех применимых объектов, которые выполняют асинхронный метод, независимо от того, подключается ли, выполняется или выполняется текущий объект.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное значение,** которое может быть [значением ObjectStateEnum.](objectstateenum.md) Значение по умолчанию **— adStateClosed.**

## <a name="remarks"></a>Заметки

Свойство State **можно** использовать для определения текущего состояния заданного объекта в любое время.

Свойство **State** объекта может иметь сочетание значений. Например, если выполняется выписка, это свойство будет иметь комбинированные значения **adStateOpen** и **adStateExecuting.**

Свойство **State** имеет только чтение.

