---
title: Свойства HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291994"
---
# <a name="helpcontext-helpfile-properties-ado"></a>Свойства HelpContext, HelpFile (ADO)

**Область применения**: Access 2013, Office 2013

Указывает файл справки и тему, связанную с [объектом Error.](error-object-ado.md)

## <a name="return-values"></a>Возвращаемые значения

- **HelpContextID** — возвращает контекстный ID в качестве значения **Long** для темы в файле справки.

- **HelpFile** — возвращает значение **String,** которое оценивается в полностью разрешенный путь к файлу справки.

## <a name="remarks"></a>Примечания

Если файл справки указан в свойстве **HelpFile,** свойство **HelpContext** используется для автоматического отображения идентифицируемой темы справки. Если нет соответствующей темы справки, свойство **HelpContext** возвращает ноль, а свойство **HelpFile** возвращает строку нулевой длины ("").

