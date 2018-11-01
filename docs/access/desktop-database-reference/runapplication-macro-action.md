---
title: Действия макроса RunApplication
TOCTitle: RunApplication Macro Action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf7e64c3c60098bf95a101773dbbb678ea5b711f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879993"
---
# <a name="runapplication-macro-action"></a>Действия макроса RunApplication


**Применимо к**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Примечание по безопасности" alt="Security note" /><strong>Примечание по безопасности</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Будьте осторожны при запуске исполняемых файлов или кода в макросах и приложениях. Исполняемые файлы или код могут использоваться для выполнения действий, которые могут скомпрометировать безопасность компьютера и данных.</td>
</tr>
</tbody>
</table>


Действие **RunApplication** позволяет выполнять Microsoft Windows и основе MS-DOS приложения, например Microsoft Excel, Microsoft Word или Microsoft PowerPoint в Microsoft Access. Например можно вставить данные электронных таблиц Excel в базы данных Access.


> [!NOTE]
> <P>
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</P>



## <a name="setting"></a>Параметр

Действие **RunApplication** использует следующий аргумент.

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
<td><p><strong>Командной строки</strong></p></td>
<td><p>Командная строка, используемая для запуска приложения (включая путь и другие необходимые параметры, такие как коммутаторы, запустите приложение в определенный режим). Введите в командной строке в поле <strong>Командная строка</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов. Обязательный аргумент.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Приложения, выбранных с помощью этого действия загружает и выполняется на переднем плане. Макрос, содержащий это действие по-прежнему производится после запуска приложения.

Можно перенести данные между приложением и доступа с помощью средства Microsoft Windows динамический обмен данными (DDE) exchange или в буфер обмена. Можно использовать действие **SendKeys** для отправки нажатия клавиш для других приложений (хотя DDE является более эффективный способ передачи данных). Также можно обмениваться данными между приложениями с помощью автоматизации.

Приложения на основе MS-DOS выполните в окне MS-DOS в среде Windows.

В операционных системах Windows существует несколько способов запуска приложения, в том числе запуск программы в проводнике Windows, с помощью команды **выполнить** в меню **Пуск** и дважды щелкните значок программы на рабочем столе Windows.

Не удается выполнить действие **RunApplication** в Visual Basic для приложений (VBA) модуля. Вместо этого используйте функцию VBA **командной консоли** .

