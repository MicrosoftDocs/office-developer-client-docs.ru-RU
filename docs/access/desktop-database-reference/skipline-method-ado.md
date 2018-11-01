---
title: Метод SkipLine (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c1ab54402dac8f6721c4c12f55f07979c4adff4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885453"
---
# <a name="skipline-method-ado"></a>Метод SkipLine (ADO)


**Применимо к**: Access 2013, Office 2013

Пропускает одну всю строку при чтении текстовый поток.

## <a name="syntax"></a>Синтаксис

*Поток*. SkipLine

## <a name="remarks"></a>Замечания

Все символы, включая Далее разделителя строки, пропускаются. По умолчанию [LineSeparator](lineseparator-property-ado.md) — **adCRLF**. При попытке пропустить [EOS](eos-property-ado.md)текущей позиции просто останется на **EOS**.

Метод **SkipLine** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).

