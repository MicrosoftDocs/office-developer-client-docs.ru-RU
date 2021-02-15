---
title: Using ADO with Scripting Languages
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312043"
---
# <a name="using-ado-with-scripting-languages"></a>Использование ADO со скриптовыми языками


**Область применения**: Access 2013, Office 2013

В среде сценариев ADO позволяет выставлять данные с помощью сценариев на стороне сервера. В этом сценарии ADO, поставщик OLE DB, который он использует, и все другие компоненты, необходимые для ссылки на заданное хранилище данных, устанавливаются на сервер со службами IIS. С ASP (ASP) ADO — это компонент, на который ссылается сценарий, который, например, может создавать HTML. Этот HTML-контент можно передать через HTTP в клиентский веб-браузер. С помощью сценариев веб-страницы могут отправлять действия обратно на серверный сценарий, позволяя обновлять, просматривать или просматривать определенные данные.

## <a name="odbc-data-sources"></a>Источники данных ODBC

Одно из важных различий между скриптами и кодом ADO без скриптов — это источник данных ODBC, если он используется. Для приложений без скриптов можно создать DSN пользователя в администраторе источника данных ODBC. Для сценариев, запущенных в IIS, необходимо создать системную DSN; в противном случае сценарии не распознают созданный источник данных. Это относится ко всем приложениям для создания скриптов ADO с помощью поставщика Microsoft OLE DB для ODBC через Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Ссылка на библиотеку ADO

Н/Д с языками сценариев.

## <a name="handling-events"></a>Обработка событий

Н/Д с языками сценариев.

В следующих темах содержатся более конкретные сведения об использовании ADO с языками сценариев:

- [JScript ADO Programming](jscript-ado-programming.md)

- [VBScript ADO Programming](vbscript-ado-programming.md)
