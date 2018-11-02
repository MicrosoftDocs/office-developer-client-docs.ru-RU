---
title: Метод SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923926"
---
# <a name="skipline-method-ado"></a>Метод SkipLine (ADO)


**Применимо к**: Access 2013, Office 2013

Пропускает одну всю строку при чтении текстовый поток.

## <a name="syntax"></a>Синтаксис

*Поток*. SkipLine

## <a name="remarks"></a>Примечания

Все символы, включая Далее разделителя строки, пропускаются. По умолчанию [LineSeparator](lineseparator-property-ado.md) — **adCRLF**. При попытке пропустить [EOS](eos-property-ado.md)текущей позиции просто останется на **EOS**.

Метод **SkipLine** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).

