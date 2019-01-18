---
title: Настройка формата маршалинга потоков DCOM
TOCTitle: Setting DCOM stream marshaling format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09463552faff9c4b74b73379385ab8ba55b4f62c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698045"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Настройка формата маршалинга потоков DCOM


**Применимо к**: Access 2013, Office 2013

Клиентский компьютер с помощью компонентов служб удаленных рабочих СТОЛОВ 1.5 или более ранней версии не совместим с сервером с использованием компонентов служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии. При использовании DCOM протоколе, поддержка для служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии более эффективно с точки зрения переноса объекты [набора записей](recordset-object-ado.md) . Если ваш клиент использует компоненты служб удаленных рабочих СТОЛОВ 1.5 или более ранней версии, можно задать сервер для работы с предыдущей Поддержка служб удаленных рабочих СТОЛОВ (называемые служб удаленных рабочих СТОЛОВ 1.0) или более поздней версии поддерживают служб удаленных рабочих СТОЛОВ (называемое служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии). Задавайте для следующие разделы реестра:

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-или -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

