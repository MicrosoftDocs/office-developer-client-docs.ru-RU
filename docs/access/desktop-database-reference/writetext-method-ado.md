---
title: Метод WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308269"
---
# <a name="writetext-method-ado"></a>Метод WriteText (ADO)

**Область применения**: Access 2013, Office 2013

Записывает указанную текстовую строку в объект [Stream](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Stream*. *Данные*WriteText, *Options*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Data* |**Строковое** значение, содержащее текст символов для записи.|
|*Параметры* |Необязательное. Значение [стреамвритинум](streamwriteenum.md) , которое указывает, должен ли символ разделителя строк записываться в конце указанной строки.|

## <a name="remarks"></a>Примечания

Указанные строки записываются в объект **Stream** без лишних пробелов или знаков между строками.

Для текущей [позиции](position-property-ado.md) задается символ, следующий за записанными данными. Метод **WriteText** не усекает остальные данные в потоке. Если вы хотите усечь эти символы, вызовите [SetEOS](seteos-method-ado.md).

Если вы пишете за пределами текущей позиции [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) [EOS](eos-property-ado.md) , размер **потока** увеличится до того, как будут содержаться новые символы, и **EOS** перейдет к новому последнему байту в **потоке**.

> [!NOTE]
> Метод **WriteText** используется с текстовыми потоками ([Type](type-property-ado-stream.md) — **адтипетекст**). Для двоичных потоков (**Type** — **Адтипебинари**) используйте [Write](write-method-ado.md).


