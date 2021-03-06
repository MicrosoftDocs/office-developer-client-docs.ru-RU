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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294136"
---
# <a name="definedsize-property-ado"></a>Свойство DefinedSize (ADO)


**Область применения**: Access 2013, Office 2013

Указывает емкость данных объекта [Field.](field-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное** значение, которое отражает определенный размер поля как количество bytes.

## <a name="remarks"></a>Примечания

Свойство **DefinedSize используется** для определения емкости данных объекта **Field.**

Свойства **DefinedSize** и [ActualSize](actualsize-property-ado.md) отличаются. Например, рассмотрим объект **Field** с объявленным типом **adVarChar** и **свойством DefinedSize** 50, содержащим один символ. Возвращаемая значения **свойства ActualSize** — это длина в bytes одного символа.

