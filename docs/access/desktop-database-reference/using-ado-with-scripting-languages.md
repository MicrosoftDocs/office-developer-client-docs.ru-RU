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

В среде скриптов ADO позволяет выставлять данные с помощью сценариев на стороне сервера. В этом сценарии ADO— поставщик OLE DB, который он использует, и все другие компоненты, необходимые для ссылки на данный хранилище данных, устанавливаются на сервере с службы IIS (IIS). С ASP (ASP) ADO — это компонент, на который ссылается скрипт, который может создавать HTML, например. Этот HTML-контент можно передать через HTTP в клиентский веб-браузер. С помощью скриптов веб-сайт может отправлять действия обратно в серверный сценарий, что позволяет обновлять, пересекать или просматривать определенные данные.

## <a name="odbc-data-sources"></a>Источники данных ODBC

Одно заметное различие между скриптами и кодом ADO без скриптов — это источник данных ODBC, если он используется. Для приложений, не создающих сценарии, можно создать DSN пользователя в администраторе источника данных ODBC. Для скриптов, работающих под IIS, необходимо создать систему DSN; в противном случае скрипты не распознают созданный источник данных. Это относится к любому приложению для скриптинга ADO с помощью поставщика DB Microsoft OLE для ODBC через Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Ссылки на библиотеку ADO

N/A с языками скриптов.

## <a name="handling-events"></a>Обработка событий

N/A с языками скриптов.

В следующих темах содержатся более конкретные сведения об использовании ADO с языками скриптов:

- [JScript ADO Programming](jscript-ado-programming.md)

- [VBScript ADO Programming](vbscript-ado-programming.md)
