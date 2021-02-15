---
title: Метод CreateParameter (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295396"
---
# <a name="createparameter-method-ado"></a>Метод CreateParameter (ADO)

**Область применения**: Access 2013, Office 2013

Создает новый объект [Parameter](parameter-object-ado.md) с указанными свойствами.

## <a name="syntax"></a>Синтаксис

**Задана** *команда*  =  *параметра*. CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **Parameter.**

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Необязательный параметр. **Строка** с именем объекта **Parameter.**|
|*Тип* |Необязательный параметр. Значение [DataTypeEnum,](datatypeenum.md) которое указывает тип данных объекта **Parameter.**|
|*Направление* |Необязательный параметр. Значение [ParameterDirectionEnum,](parameterdirectionenum.md) которое указывает тип **объекта Parameter.**|
|*Размер* |Необязательный параметр. **Длинное** значение, которое указывает максимальную длину значения параметра в символах или в ветвях.|
|*Значение* |Необязательный параметр. **Вариант,** который указывает значение для объекта **Parameter.**|

## <a name="remarks"></a>Заметки

Используйте метод **CreateParameter** для создания объекта **Parameter** с указанным именем, типом, направлением, размером и значением. Любые значения, которые вы передаете в аргументы, будут записаны в соответствующие **свойства parameter.**

Этот метод не включает автоматически объект **Parameter** в коллекцию **Parameters** объекта [Command.](command-object-ado.md) Это позволяет установить дополнительные свойства, значения которых ADO будет проверять при добавлении объекта **Parameter** в коллекцию.

При указании типа данных переменной длины в аргументе *Type* необходимо либо передать аргумент *Size,* либо задать свойство [Size](size-property-ado.md) объекта **Parameter** перед его приложением в коллекцию **Parameters;** в противном случае возникает ошибка.

Если в аргументе *Type* указан числовой тип данных **(adNumeric** или **adDecimal),** необходимо также задать свойства [NumericScale](numericscale-property-ado.md) и [Precision.](precision-property-ado.md)

