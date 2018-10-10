---
title: DefinedSize Property (ADO)
TOCTitle: DefinedSize Property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8ffd8bb24abcab737ebc4bb23a0af717c02d486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480336"
---
# <a name="definedsize-property-ado"></a>DefinedSize Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает объем данных объекта [поля](field-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , отражает определенный размер поля в байтах.

## <a name="remarks"></a>Замечания

Свойство **DefinedSize** используется для определения емкости данных объекта **поля** .

Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) не совпадают. Например рассмотрим объект **Field** с типом объявленные **adVarChar** и значение свойства **DefinedSize** 50, содержащий один символ. **ActualSize** свойство возвращает значение длины в байтах один символ.

