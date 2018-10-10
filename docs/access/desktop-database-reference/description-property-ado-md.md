---
title: Description Property (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29c6723d710fcf3a8114fb4460326d87261c3fc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480472"
---
# <a name="description-property-ado-md"></a>Description Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Возвращает описание текста текущего объекта.

## <a name="return-values"></a>Return Values

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Замечания

Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы. **Описание** возвращает пустую строку ("») для всех остальных типов элементов. Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.

Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

