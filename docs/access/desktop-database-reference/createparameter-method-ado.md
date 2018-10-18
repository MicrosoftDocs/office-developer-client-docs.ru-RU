---
title: CreateParameter Method (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 00a2c5e2eb8613434b80c80e2a51cbf5d1deb644
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605487"
---
# <a name="createparameter-method-ado"></a>CreateParameter Method (ADO)


**Применимо к**: Access 2013 | Office 2013


Создает новый объект [параметр](parameter-object-ado.md) с указанными свойствами.

## <a name="syntax"></a>Синтаксис

**Установка** *параметр*  =  *команды*. CreateParameter (*имя*, *Тип*, *направление*, *размер*, *значение*)

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает объект **параметра** .

## <a name="parameters"></a>Параметры

  - *Имя*

  - Необязательный параметр. **Строковое** значение, содержащее имя объекта **параметра** .

  - *Тип*

  - Необязательный параметр. [DataTypeEnum](datatypeenum.md) значение, задающее тип данных **параметра** объекта.

  - *Direction*

  - Необязательный параметр. [ParameterDirectionEnum](parameterdirectionenum.md) значение, задающее тип объекта **параметра** .

  - *Размер*

  - Необязательный параметр. Значение типа **Long** , определяет максимальную длину значения параметра в символы или в байтах.

  - *Значение*

  - Необязательный параметр. **Variant** , который задает значение для **параметра** объекта.

## <a name="remarks"></a>Замечания

Используйте метод **CreateParameter** для создания нового объекта **параметра** с указанным именем, типом, направление, размер и значение. Все значения, передаваемого в аргументах записываются в соответствующие свойства **параметра** .

Этот метод не добавляет автоматически объект **параметра** в коллекцию **параметров** объекта [Command](command-object-ado.md) . Это позволяет задавать дополнительные свойства, чьи значения ADO будет проверять при добавьте объект **параметра** в коллекцию.

Если указан тип данных переменной длины в аргументе *типа* , необходимо передать аргумент *размер* или задать свойство [размер](size-property-ado.md) объекта **параметра** перед добавлением в коллекцию **параметров** ; в противном случае возникает ошибка.

При указании числовым типом данных (**adNumeric** или **adDecimal**) в качестве аргумента *типа* , необходимо также установить свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) .

