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

В среде сценариев ADO позволяет предоставлять данные с помощью серверных скриптов. В этом сценарии ADO, используемый поставщик OLE DB, который он использует, и все остальные компоненты, необходимые для ссылки на данное хранилище данных, устанавливаются на сервер, на котором выполняются службы IIS. С помощью ASP (Active Server Pages) ADO является компонентом, на который ссылается скрипт, который может создавать HTML, например. Это содержимое HTML может передаваться через HTTP в клиентский веб-браузер. С помощью сценариев веб-страница может отправлять действия обратно на серверный сценарий, позволяя обновлять, просматривать и просматривать определенные данные.

## <a name="odbc-data-sources"></a>Источники данных ODBC

Важным различием между сценариями и кода ADO без написания скриптов является источник данных ODBC, если он используется. Для приложений, не использующих сценарии, можно создать пользовательское имя DSN в администраторе источника данных ODBC. Для сценариев, выполняемых в службах IIS, необходимо создать системный DSN. в противном случае ваши скрипты не смогут распознать созданный вами источник данных. Это относится ко всем приложениям сценариев ADO с помощью поставщика Microsoft OLE DB для ODBC через Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Создание ссылок на библиотеку ADO

N/A с языками сценариев.

## <a name="handling-events"></a>Обработка событий

N/A с языками сценариев.

В следующих разделах содержатся более конкретные сведения об использовании ADO с языками сценариев:

- [JScript ADO Programming](jscript-ado-programming.md)

- [VBScript ADO Programming](vbscript-ado-programming.md)
