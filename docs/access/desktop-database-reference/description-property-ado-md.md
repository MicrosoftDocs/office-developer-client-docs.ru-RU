---
title: Свойство Description (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96f3762df84f2534b31501bdf44059152e7077bb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873154"
---
# <a name="description-property-ado-md"></a>Свойство Description (ADO MD)


**Применимо к**: Access 2013, Office 2013

Возвращает описание текста текущего объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Замечания

Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы. **Описание** возвращает пустую строку ("») для всех остальных типов элементов. Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.

Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

