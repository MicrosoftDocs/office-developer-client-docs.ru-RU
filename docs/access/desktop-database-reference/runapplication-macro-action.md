---
title: Макрокоманда RunApplication
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306841"
---
# <a name="runapplication-macro-action"></a>Макрокоманда RunApplication

**Область применения**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Заметка о безопасности" alt="Security note" /><strong>Заметка о безопасности</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Будьте осторожны при запуске исполняемых файлов или кода в макросах и приложениях. Исполняемые файлы или код могут использоваться для выполнения действий, которые могут скомпрометировать безопасность компьютера и данных.</td>
</tr>
</tbody>
</table>

Вы можете использовать действие **рунаппликатион** для запуска приложений на основе Microsoft Windows или MS DOS, таких как Microsoft Excel, Microsoft Word или Microsoft PowerPoint, в Microsoft Access. Например, вам может потребоваться вставить данные электронной таблицы Excel в базу данных Access.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметры

Действие **рунаппликатион** имеет следующий аргумент.

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
<td><p><strong>Командная строка</strong></p></td>
<td><p>Командная строка, используемая для запуска приложения (включая путь и другие необходимые параметры, такие как параметры, которые запускают приложение в определенном режиме). Введите командную строку в поле <strong>командНая строка</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов. Обязательный аргумент.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Приложение, выбранное с этим действием, загружается и выполняется на переднем плане. Макрос, содержащий это действие, продолжает работу после запуска приложения.

Вы можете передавать данные между другим приложением и Access с помощью средства Microsoft Windows Dynamic Data Exchange (DDE) или буфера обмена. Вы можете использовать макрокоманду **SendKeys** для отправки нажатий клавиш в другое приложение (хотя DDE является более эффективным способом передачи данных). Вы также можете обмениваться данными между приложениями с помощью автоматизации.

Приложения, работающие под управлением MS DOS, выполняются в окне MS-DOS в среде Windows.

В операционных системах Windows существует несколько способов запуска приложения, в том числе запуска программы из проводника Windows, с помощью команды **выполнить** в меню " **Пуск** " и двойным нажатием значка программы на рабочем столе Windows.

Вы не можете выполнить действие **рунаппликатион** в модуле Visual Basic для приложений (VBA). Вместо этого используйте функцию **оболочки** VBA.

