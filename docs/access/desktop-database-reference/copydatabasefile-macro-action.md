---
title: CopyDatabaseFile Macro Action
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482737"
---
# <a name="copydatabasefile-macro-action"></a>CopyDatabaseFile Macro Action


**Применимо к**: Access 2013 | Office 2013

**КопироватьФайлБазыДанных** можно использовать для создания копии текущего Microsoft SQL Server 7.0 или более поздняя версия базы данных, подключенные к проект Microsoft Access. Access отключает текущую базу данных и подключает ее к конечному серверу. Дополнительные сведения о присоединение и отсоединение базы данных SQL Server см.


> [!NOTE]
> <P>
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</P>



## <a name="setting"></a>Параметр

**КопироватьФайлБазыДанных** имеет следующие аргументы.

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
<td><p><strong>Имя файла базы данных</strong></p></td>
<td><p>Имя нового файла данных образец. Путь по умолчанию является текущее расположение файла проекта Microsoft Access (файлы с расширением ADP).</p></td>
</tr>
<tr class="even">
<td><p><strong>Перезапись существующего файла</strong></p></td>
<td><p>Указывает, следует ли заменить существующий файл с тем же именем. Если значение <strong>Да</strong> и имя файла уже существует, файл перезаписывается. Если значение <strong>Нет</strong> и имя файла уже существует, файл не перезаписывается и не удается выполнить действие. Если файл еще не существует, этот параметр игнорируется. По умолчанию используется значение <strong>Да</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Отключите всех пользователей</strong></p></td>
<td><p>Указывает, следует ли доступа принудительное отключение базы данных пользователей. Если параметр имеет значение <strong>Yes</strong>, все пользователи, подключенные к текущей базе данных не соединены по сети, чтобы операции копирования базы данных можно продолжить. Если значение <strong>No</strong> , а один или несколько пользователей подключены к базе данных, возникает ошибка операции копирования базы данных. Значение по умолчанию: <strong>Нет</strong>.</p>

> [!WARNING]
> <P>Отключение пользователей из базы данных без предварительного предупреждения может привести к потере данных.</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Операция копирования является синхронным, поэтому не могут выполнять другие операции до завершения копии базы данных.

**КопироватьФайлБазыДанных** не только копирование данных, определений данных и объектов базы данных, но также копирует расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значений подстановки.

Требования для копирования базы данных:

  - Перед копированием файла базы данных, необходимо отключить все приложения и пользователи.

  - Необходимо закрыть все объекты и представлений, за исключением области навигации.

  - Текущей базы данных не должна быть реплицирована.

  - Базы данных-источника сервера должны быть Microsoft SQL Server версии 7.0 или более поздней версии или SQL Server 2000 Desktop Engine на локальном компьютере.

<!-- end list -->

  - База данных SQL Server на исходном сервере должен быть один файл базы данных.

  - Необходимо быть членом роли sysadmin на исходном и целевом компьютерах SQL Server.

Чтобы запустить **КопироватьФайлБазыДанных** в Visual Basic для приложений модуль, используйте метод **CopyDatabaseFile** **объекта** .
