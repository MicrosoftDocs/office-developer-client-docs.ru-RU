---
title: Свойство Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf0e9751e822e5ff2250a15138546678deb76bc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921098"
---
# <a name="description-property-ado-md"></a>Свойство Description (ADO MD)


**Применимо к**: Access 2013, Office 2013

Возвращает описание текста текущего объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Примечания

Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы. **Описание** возвращает пустую строку ("») для всех остальных типов элементов. Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.

Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

