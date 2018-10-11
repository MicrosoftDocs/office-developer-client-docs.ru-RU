---
title: LineSeparator Property (ADO)
TOCTitle: LineSeparator Property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1aee67410e2abf921bdbd61e6cd8573e090fafd9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481771"
---
# <a name="lineseparator-property-ado"></a>LineSeparator Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает двоичных символов для использования в качестве разделителя строки в объектах [потока](stream-object-ado.md) текста.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает [LineSeparatorsEnum](lineseparatorsenum.md) значение, указывающее знак разделителя строки, используемые в **поток**. Значение по умолчанию — **adCRLF**.

## <a name="remarks"></a>Замечания

**LineSeparator** используется для интерпретации строки при чтении содержимое текста **потока**. С помощью метода [SkipLine](skipline-method-ado.md) можно пропустить строки.

**LineSeparator** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**). Это свойство игнорируется, если **Тип** — **adTypeBinary**.

