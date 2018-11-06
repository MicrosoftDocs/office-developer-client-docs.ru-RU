---
title: Макрокоманда OpenDiagram
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b04870a416874e2136e21b40c62d8e64a6182efe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998548"
---
# <a name="opendiagram-macro-action"></a>Макрокоманда OpenDiagram

**Применимо к**: Access 2013, Office 2013

В проекте Microsoft Access можно использовать действие **OpenDiagram** для открытия схемы базы данных в режиме конструктора.

> [!NOTE]
> Это действие не разрешено, если база данных не является доверенной. 

## <a name="setting"></a>Параметр

Действие **OpenDiagram** использует следующий аргумент.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Имя схемы</strong></p></td>
<td><p>Имя схемы базы данных, чтобы открыть. В поле <strong>Имя схемы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показывает все схемы базы данных в текущей базе данных. Обязательный аргумент. Если макрос, содержащий <strong>OpenDiagram</strong> действие в базе данных библиотеки, Microsoft Access сначала выполняет поиск схемы с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

Это действие аналогично дважды щелкнув схемы базы данных в области навигации или щелкнув правой кнопкой мыши на схеме базы данных в области навигации и затем выбрав **Представление конструирования**.

> [!TIP]
> Схемы базы данных можно перетаскивать из области переходов в строку действие в макросе. Это автоматически создает **ОткрытьСхему открывает схему базы данных в режиме конструктора** .

Чтобы выполнить действие **OpenDiagram** в Visual Basic для приложений (VBA) модуль, используйте метод **OpenDiagram** **объекта** .

