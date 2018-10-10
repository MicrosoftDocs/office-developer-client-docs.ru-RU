---
title: Using ADO with Scripting Languages
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2de5cd9507ede3308a207b078a5bc66a4917e267
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483102"
---
# <a name="using-ado-with-scripting-languages"></a>Using ADO with Scripting Languages


**Применимо к**: Access 2013 | Office 2013

В среде сценариев ADO позволяет предоставлять данные путем получения сценариев на стороне сервера. В этом сценарии ADO, соответствующий поставщик OLE DB, который использует и других компонентов, необходимых для ссылки хранилища данных установлены на сервере под управлением Internet Information Services (IIS). С помощью Active Server Pages (ASP), ADO — это компонент, указанный в скрипте, который можно создать HTML-код, например. В этом HTML-содержимое может быть передан по протоколу HTTP веб-браузере клиента. Посредством использования сценариев, веб-странице можно отправить действия обратно в скрипт на сервере, что позволяет обновить, проходят через или просмотра определенных данных.

## <a name="odbc-data-sources"></a>Источники данных ODBC

Один важные различия между сценариев и не являющиеся скрипты кода ADO является источником данных ODBC при использовании. Для приложений, не являющиеся сценариев можно создать пользовательский DSN в источники данных ODBC. Для сценариев, работающих под управлением служб IIS необходимо создать DSN системы; в противном случае сценарии не распознает источника данных, которую вы создали. Это относится к любой ADO сценариев приложения с помощью поставщик Microsoft OLE DB для ODBC через Microsoft IIS.

## <a name="referencing-the-ado-library"></a>Создание ссылок на библиотеку ADO

Н/д с языками сценариев.

## <a name="handling-events"></a>Обработка событий

Н/д с языками сценариев.

В следующих разделах содержится более подробные сведения об использовании ADO с языками сценариев:

  - [ADO в VBScript](vbscript-ado-programming.md)

  - [ADO в JScript](jscript-ado-programming.md)

