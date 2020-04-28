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

*Команда*" **задать** *параметр* = ". CreateParameter (*имя*, *Тип*, *направление*, *Размер*, *значение*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **Parameter** .

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Необязательное. **Строковое** значение, содержащее имя объекта **Parameter** .|
|*Тип* |Необязательное. Значение [DataTypeEnum](datatypeenum.md) , задающее тип данных объекта **Parameter** .|
|*Направление* |Необязательное. Значение [параметердиректионенум](parameterdirectionenum.md) , задающее тип объекта **Parameter** .|
|*Размер* |Необязательное. **Длинное** значение, задающее максимальную длину значения параметра в символах или байтах.|
|*Значение* |Необязательное. Значение **Variant** , задающее значение для объекта **Parameter** .|

## <a name="remarks"></a>Примечания

Используйте метод **CreateParameter** , чтобы создать новый объект **Parameter** с указанным именем, типом, направлением, размером и значением. Все значения, передаваемые в аргументы, записываются в соответствующие свойства **параметра** .

Этот метод не добавляет автоматически объект **Parameter** в коллекцию **Parameters** объекта [Command](command-object-ado.md) . Это позволяет задать дополнительные свойства, значения которых будут проверяться с помощью ADO при добавлении объекта **Parameter** в коллекцию.

Если указать тип данных переменной длины в аргументе *типа* , необходимо либо передать аргумент *размера* , либо задать свойство [size](size-property-ado.md) объекта **Parameter** перед добавлением его в коллекцию **Parameters** ; в противном случае возникает ошибка.

Если указать числовой тип данных (**аднумерик** или **аддеЦимал**) в аргументе *Type* , необходимо также задать свойства [NumericScale](numericscale-property-ado.md) и [Precision](precision-property-ado.md) .

