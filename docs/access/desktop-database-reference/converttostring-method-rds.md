---
title: Метод ConvertToString (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c589339eb838f944ce4443c19a787eafb01c3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295515"
---
# <a name="converttostring-method-rds"></a>Метод ConvertToString (RDS)

**Область применения**: Access 2013, Office 2013 

Преобразует набор [записей в](recordset-object-ado.md) строку MIME, которая представляет данные наборов записей.

## <a name="syntax"></a>Синтаксис

*DataFactory*. ConvertToString *(Набор записей)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataFactory* |Переменная объекта, представляют [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)|
|*Recordset* |Переменная объекта, представляют объект **Recordset.**|

## <a name="remarks"></a>Примечания

С помощью файлов .asp используйте **ConvertToString** для встраив набор **записей** на страницу HTML, созданную на сервере, чтобы транспортировать ее на клиентский компьютер.

**ConvertToString** сначала загружает набор **записей** в таблицы службы Cursor, а затем создает поток в формате MIME.

На клиенте служба удаленных данных может преобразовать строку MIME обратно в полностью функционируюющий **набор записей.** Он хорошо работает для обработки менее 400 строк данных с шириной не более 1024 bytes на строку. Не следует использовать его для потоковой передачи данных BLOB и больших наборов результатов по HTTP. На строке не выполняется сжатие проводов, поэтому очень большие наборы данных будут проходить через HTTP по сравнению с форматом таблицы, оптимизированной по проводам, определенным и развернутым службой удаленных данных в качестве своего родного формата протокола транспорта.

> [!NOTE]
> Если вы используете ASP, чтобы встраить в клиентскую HTML-страницу строку MIME, следует помнить, что версии VBScript раньше версии 2.0 ограничивают размер строки 32K. Если это ограничение превышено, возвращается ошибка. При использовании MIME-встраивке с помощью файлов asp область запроса должна быть относительно небольшой. Чтобы исправить это, скачайте последнюю версию VBScript из [Центра загрузки Майкрософт.](https://www.microsoft.com/download/default.aspx)


