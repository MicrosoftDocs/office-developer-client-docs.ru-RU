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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717729"
---
# <a name="converttostring-method-rds"></a>Метод ConvertToString (RDS)

**Применимо к**: Access 2013, Office 2013 

Преобразование [набора записей](recordset-object-ado.md) MIME строку, представляющую данных набора записей.

## <a name="syntax"></a>Синтаксис

*DataFactory*. ConvertToString (*записей*)

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*DataFactory* |Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .|
|*Recordset* |Объектная переменная, представляющий объект **набора записей** .|

## <a name="remarks"></a>Замечания

С помощью ASP-файлы используйте **ConvertToString** внедрение **записей** в HTML-страницу, созданный на сервере для передачи его на клиентский компьютер.

**ConvertToString** сначала загружает **записей** в таблицы службы курсора и создает потока в формате MIME.

В клиенте удаленной службы данные можно преобразовать строку MIME обратно в полностью функциональный **набор записей**. Хорошо подходит для обработки не более 400 строк данных с не более чем 1024 байта ширину каждой строки. Вы не следует использовать для потоковой передачи данных больших двоичных ОБЪЕКТОВ и задает больших результатов по протоколу HTTP. Без сжатия проводов выполняется в строке, очень большие наборы данных занять значительное время в транспорт по протоколу HTTP, по сравнению с формат optimized проводов tablegram определены и развернуты с удаленной службы данных его в формате собственного транспортный протокол.

> [!NOTE]
> При использовании страницы ASP внедрение результирующую строку MIME в HTML-страницу клиента, обратите внимание, что версии VBScript, предшествующие версии 2.0 ограничение на размер строки 32 КБ. Если это ограничение превышено, возвращается ошибка. Сохранение небольшого области запроса при использовании внедрение MIME с помощью ASP-файлы. Чтобы устранить эту проблему, загрузите последнюю версию VBScript из [Центра загрузки Майкрософт](https://www.microsoft.com/download/default.aspx).


