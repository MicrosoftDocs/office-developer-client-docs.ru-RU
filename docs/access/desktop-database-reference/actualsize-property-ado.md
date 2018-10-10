---
title: ActualSize Property (ADO)
TOCTitle: ActualSize Property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0fa7b4f5fe27c25db51338dd1dfd1a68a936364
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479776"
---
# <a name="actualsize-property-ado"></a>ActualSize Property (ADO)

**Применимо к**: Access 2013 | Office 2013

Фактическая длина значения поля.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Возвращает значение типа **Long** . Некоторые поставщики могут разрешить это свойство должно быть задано для резервирования пространства для данных больших двоичных ОБЪЕКТОВ, в котором case значение по умолчанию равно 0.

## <a name="remarks"></a>Замечания

Свойство **ActualSize** возвращает фактический длины значения объекта [поля](field-object-ado.md) . Для всех полей **ActualSize** свойство доступно только для чтения. Если ADO не может быть определен значение **поля** объекта, свойство **ActualSize** возвращает **adUnknown**.

Свойства **ActualSize** и [DefinedSize](definedsize-property-ado.md) отличаются, как показано в следующем примере. Объект **Field** с типом объявленные **adVarChar** и максимальную длину 50 символов возвращает значение свойства **DefinedSize** 50, но она возвращает значение свойства **ActualSize** — это длина данных, сохраненных в процессе работы Текущая запись. **Поля** с **DefinedSize** быстрее, чем 255 байт обрабатывается как столбцы переменной длины.

