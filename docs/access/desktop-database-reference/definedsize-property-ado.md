---
title: Свойство DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715328"
---
# <a name="definedsize-property-ado"></a>Свойство DefinedSize (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает объем данных объекта [поля](field-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , отражает определенный размер поля в байтах.

## <a name="remarks"></a>Замечания

Свойство **DefinedSize** используется для определения емкости данных объекта **поля** .

Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) не совпадают. Например рассмотрим объект **Field** с типом объявленные **adVarChar** и значение свойства **DefinedSize** 50, содержащий один символ. **ActualSize** свойство возвращает значение длины в байтах один символ.

