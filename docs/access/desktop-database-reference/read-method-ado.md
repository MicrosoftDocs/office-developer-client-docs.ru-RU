---
title: Метод Read — объекты данных ActiveX (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307674"
---
# <a name="read-method-ado"></a>Метод Read (ADO)

**Область применения**: Access 2013, Office 2013

Считывает указанное число байтов из двоичного объекта [Stream](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Variant* = *Поток*Variant. Read (*нумбитес* )

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*нумбитес* |Необязательное. **Длинное** значение, задающее количество байтов для чтения из файла или значение [стреамреаденум](streamreadenum.md) **адреадалл**, используемое по умолчанию.|

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает указанное число байтов или весь поток из объекта **Stream** и возвращает полученные данные в виде **Variant**.

## <a name="remarks"></a>Примечания

Если *нумбитес* больше, чем число байтов, оставшихся в **потоке**, возвращаются только оставшиеся байты. Прочитанные данные не дополняются в соответствии с длиной, указанной в параметре *нумбитес*. Если не осталось байтов для чтения, возвращается Variant со значением NULL. **Read** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> *Нумбитес* всегда измеряется в байтах. Для объектов текстовых **потоков** ([Type](type-property-ado-stream.md) — **адтипетекст**) используйте [ReadText](readtext-method-ado.md).


