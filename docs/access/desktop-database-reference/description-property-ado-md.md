---
title: Свойство Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293940"
---
# <a name="description-property-ado-md"></a>Свойство Description (ADO MD)


**Область применения**: Access 2013, Office 2013

Возвращает текстовое описание текущего объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступна только для чтения.

## <a name="remarks"></a>Замечания

Для объектов [member](member-object-ado-md.md) **Описание** применяется только к элементам Measure и Measure. **Description** возвращает пустую строку ("") для всех других типов элементов. Дополнительные сведения о различных типах членов можно узнать в свойстве [Type](type-property-ado-md.md) .

Это свойство поддерживается только для объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) . При обращении к этому свойству из объектов **member** , принадлежащих объекту [position](position-object-ado-md.md) , возникает ошибка.

