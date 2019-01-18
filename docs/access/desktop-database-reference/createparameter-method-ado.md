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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700684"
---
# <a name="createparameter-method-ado"></a>Метод CreateParameter (ADO)

**Применимо к**: Access 2013, Office 2013

Создает новый объект [параметр](parameter-object-ado.md) с указанными свойствами.

## <a name="syntax"></a>Синтаксис

**Установка** *параметр*  =  *команды*. CreateParameter (*имя*, *Тип*, *направление*, *размер*, *значение*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **параметра** .

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Name* |Необязательно. **Строковое** значение, содержащее имя объекта **параметра** .|
|*Type* |Необязательно. [DataTypeEnum](datatypeenum.md) значение, задающее тип данных **параметра** объекта.|
|*Direction* |Необязательно. [ParameterDirectionEnum](parameterdirectionenum.md) значение, задающее тип объекта **параметра** .|
|*Size* |Необязательно. Значение типа **Long** , определяет максимальную длину значения параметра в символы или в байтах.|
|*Value* |Необязательно. **Variant** , который задает значение для **параметра** объекта.|

## <a name="remarks"></a>Замечания

Используйте метод **CreateParameter** для создания нового объекта **параметра** с указанным именем, типом, направление, размер и значение. Все значения, передаваемого в аргументах записываются в соответствующие свойства **параметра** .

Этот метод не добавляет автоматически объект **параметра** в коллекцию **параметров** объекта [Command](command-object-ado.md) . Это позволяет задавать дополнительные свойства, чьи значения ADO будет проверять при добавьте объект **параметра** в коллекцию.

Если указан тип данных переменной длины в аргументе *типа* , необходимо передать аргумент *размер* или задать свойство [размер](size-property-ado.md) объекта **параметра** перед добавлением в коллекцию **параметров** ; в противном случае возникает ошибка.

При указании числовым типом данных (**adNumeric** или **adDecimal**) в качестве аргумента *типа* , необходимо также установить свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) .

