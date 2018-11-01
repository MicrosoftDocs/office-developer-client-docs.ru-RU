---
title: Метод SetEOS (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 420d614d100ed156b794e92f77df2e7a4180c9fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872433"
---
# <a name="seteos-method-ado"></a>Метод SetEOS (ADO)


**Применимо к**: Access 2013, Office 2013

Задает позицию за конец потока.

## <a name="syntax"></a>Синтаксис

*Поток*. SetEOS

## <a name="remarks"></a>Замечания

**SetEOS** обновляет значение свойства [EOS](eos-property-ado.md) , сделав текущую [позицию](position-property-ado.md) в конец потока. Любой байт или после текущего положения знаков усекаются.

С момента [написания](write-method-ado.md), [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не удалять любые дополнительные значения в существующие объекты **потока** , задав новое место окончания потока с **SetEOS**можно усекать этих байт или символов.


> [!WARNING]
> <P>Если значение <STRONG>EOS</STRONG> позицию перед фактический конец потока, будут потеряны все данные после новую позицию <STRONG>EOS</STRONG> .</P>


