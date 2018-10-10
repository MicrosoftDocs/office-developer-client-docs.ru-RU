---
title: ConvertToString Method (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa1a4326cf318a9cbcddf8ebcdf584543ac8ebfb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482527"
---
# <a name="converttostring-method-rds"></a>ConvertToString Method (RDS)


**Применимо к**: Access 2013 | Office 2013 

Преобразование [набора записей](recordset-object-ado.md) MIME строку, представляющую данных набора записей.

## <a name="syntax"></a>Синтаксис

*DataFactory*. ConvertToString (*записей*)

## <a name="parameters"></a>Параметры

  - *DataFactory*

  - Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .

  - *Набор записей*

  - Объектная переменная, представляющий объект **набора записей** .

## <a name="remarks"></a>Замечания

С помощью ASP-файлы используйте **ConvertToString** внедрение **записей** в HTML-страницу, созданный на сервере для передачи его на клиентский компьютер.

**ConvertToString** сначала загружает **записей** в таблицы службы курсора и создает потока в формате MIME.

В клиенте удаленной службы данные можно преобразовать строку MIME обратно в полностью функциональный **набор записей**. Хорошо подходит для обработки не более 400 строк данных с не более чем 1024 байта ширину каждой строки. Вы не следует использовать для потоковой передачи данных больших двоичных ОБЪЕКТОВ и задает больших результатов по протоколу HTTP. Без сжатия проводов выполняется в строке, очень большие наборы данных занять значительное время в транспорт по протоколу HTTP, по сравнению с формат optimized проводов tablegram определены и развернуты с удаленной службы данных его в формате собственного транспортный протокол.


> [!NOTE]
> <P>При использовании страницы ASP внедрение результирующую строку MIME в HTML-страницу клиента, обратите внимание, что версии VBScript, предшествующие версии 2.0 ограничение на размер строки 32 КБ. Если это ограничение превышено, возвращается ошибка. Сохранение небольшого области запроса при использовании внедрение MIME с помощью ASP-файлы. Чтобы устранить эту проблему, загрузите последнюю версию VBScript из <A href="https://www.microsoft.com/downloads/en/default.aspx">Центра загрузки Майкрософт</A>.</P>


