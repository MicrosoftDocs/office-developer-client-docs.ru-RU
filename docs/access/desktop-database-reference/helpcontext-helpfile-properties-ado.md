---
title: HelpContext, HelpFile Properties (ADO)
TOCTitle: HelpContext, HelpFile Properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23823ec18b4b87306fa852ac5b0b18e89f60d057
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482452"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, HelpFile Properties (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает файл справки и раздел, связанный с объектом [Ошибка](error-object-ado.md) .

## <a name="return-values"></a>Return Values

  - **HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.

  - **Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.

## <a name="remarks"></a>Замечания

Если в свойство **HelpFile** указан файл справки, свойство **HelpContext** используется для отображения раздела справки, он определяет автоматически. Если нет ни один соответствующий раздел справки, свойство **HelpContext** возвращает нуль и свойство **HelpFile** возвращает строку нулевой длины (»»).

