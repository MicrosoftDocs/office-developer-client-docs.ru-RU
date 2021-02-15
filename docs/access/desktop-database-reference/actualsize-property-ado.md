---
title: Свойство ActualSize (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280434"
---
# <a name="actualsize-property-ado"></a>Свойство ActualSize (ADO)

**Область применения**: Access 2013, Office 2013

Указывает фактическую длину значения поля.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Возвращает **длинное** значение. Некоторые поставщики могут разрешить этому свойству резервировать место для данных BLOB, в этом случае значение по умолчанию — 0.

## <a name="remarks"></a>Заметки

Используйте свойство **ActualSize** для возврата фактической длины значения объекта [Field.](field-object-ado.md) Для всех полей свойство **ActualSize** имеет только чтение. Если ADO не удается определить длину значения **объекта Field,** свойство **ActualSize** возвращает **adUnknown**.

Свойства **ActualSize** [и DefinedSize](definedsize-property-ado.md) отличаются. Объект **Field** с объявленным типом **adVarChar** и длиной не более 50 символов возвращает значение свойства **DefinedSize** 50, но возвращаемая величина свойства **ActualSize** является длиной данных, хранимых в поле для текущей записи. **Поля** с **значением DefinedSize** больше 255байт обрабатываются как столбцы переменной длины.

