---
title: Свойства HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a9ad8c700b0b0ae293683f7b79062a0edf7775f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881372"
---
# <a name="helpcontext-helpfile-properties-ado"></a>Свойства HelpContext, HelpFile (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает файл справки и раздел, связанный с объектом [Ошибка](error-object-ado.md) .

## <a name="return-values"></a>Возвращаемые значения

- **HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.

- **Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.

## <a name="remarks"></a>Замечания

Если в свойство **HelpFile** указан файл справки, свойство **HelpContext** используется для отображения раздела справки, он определяет автоматически. Если нет ни один соответствующий раздел справки, свойство **HelpContext** возвращает нуль и свойство **HelpFile** возвращает строку нулевой длины (»»).

