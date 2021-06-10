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

**Задана**   =  *команда параметров*. CreateParameter *(Имя,* *Тип,* *Направление,* *Размер*, *Значение*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **Parameter.**

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Необязательный параметр. Значение **String,** содержаное имя объекта **Параметр.**|
|*Тип* |Необязательный параметр. Значение [DataTypeEnum,](datatypeenum.md) которое указывает тип данных объекта **Parameter.**|
|*Направление* |Необязательный параметр. Значение [ParameterDirectionEnum,](parameterdirectionenum.md) которое указывает тип **объекта Parameter.**|
|*Размер* |Необязательный параметр. **Длинное** значение, которое указывает максимальную длину значения параметра в символах или bytes.|
|*Значение* |Необязательный параметр. **Вариант,** который указывает значение объекта **Параметр.**|

## <a name="remarks"></a>Примечания

Используйте метод **CreateParameter** для создания нового объекта **Parameter** с заданным именем, типом, направлением, размером и значением. Любые значения, которые вы передаете в аргументах, записаны в соответствующие свойства **параметра.**

Этот метод автоматически не привносим объект **Parameter** в коллекцию **Параметры** объекта [Command.](command-object-ado.md) Это позволяет задать дополнительные свойства, значения которых ADO будет проверять при добавлении объекта **Parameter** в коллекцию.

Если в аргументе Type указывается  тип данных переменной длины, необходимо либо передать аргумент *Size,* либо задать свойство [Size](size-property-ado.md) объекта **Parameter** перед его примесями к коллекции **Параметры;** в противном случае возникает ошибка.

Если в аргументе *Type* указывается числовой тип данных **(adNumeric** или **adDecimal),** необходимо также задать свойства [NumericScale](numericscale-property-ado.md) и [Precision.](precision-property-ado.md)

