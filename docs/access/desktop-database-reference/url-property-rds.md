---
title: Свойство URL (Справочник по базам данных для рабочих столов RDS)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313400"
---
# <a name="url-property-rds"></a>Свойство URL (RDS)

**Область применения**: Access 2013, Office 2013

Указывает строку, содержащую относительный или абсолютный URL-адрес.

Свойство **URL** можно задать во время конструирования в теге объекта [элемента управления](datacontrol-object-rds.md) DataObject или во время выполнения в коде скрипта.

## <a name="syntax"></a>Синтаксис

Время конструирования \<: param Name = "URL" значение = "Server"\>

Время выполнения: Control. URL = "Server"

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Server* |**Строковое** значение, содержащее допустимый URL-адрес.|
|*DataControl* |Объектная переменная, представляющая объект **управления** DataObject.|

## <a name="remarks"></a>Примечания

Как правило, URL-адрес определяет активный файл страницы сервера (ASP), который может создавать и возвращать [набор записей](recordset-object-ado.md). Таким образом, пользователь может получить **набор записей** , не выполняя серверный объект [данных DataObject или](datafactory-object-rdsserver.md) запрограммировать настраиваемый бизнес-объект.

Если задано свойство **URL** , [SubmitChanges](submitchanges-method-rds.md) отправит изменения в расположении, указанном с помощью URL-адреса.

