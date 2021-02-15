---
title: Свойство LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289951"
---
# <a name="lineseparator-property-ado"></a>Свойство LineSeparator (ADO)


**Область применения**: Access 2013, Office 2013

Указывает двоичный символ, который будет использоваться в качестве различиватора линии в текстовых [объектах Stream.](stream-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает [значение LineSeparatorsEnum,](lineseparatorsenum.md) которое указывает знак разлиения строки, используемый в **Stream.** Значение по умолчанию **— adCRLF.**

## <a name="remarks"></a>Заметки

**LineSeparator** используется для интерпретации строк при чтении содержимого текстового **потока.** Строки можно пропустить с помощью метода [SkipLine.](skipline-method-ado.md)

**LineSeparator** используется только с текстовыми объектами **Stream** ([Тип](type-property-ado-stream.md) **adTypeText).** Это свойство игнорируется, **если type** **— adTypeBinary.**

