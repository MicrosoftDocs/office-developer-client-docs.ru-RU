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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308668"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Настройка формата маршалинга потоков DCOM


**Область применения**: Access 2013, Office 2013

Клиентский компьютер, использующий компоненты из RDS 1.5 или ранее, не совместим с сервером с использованием компонентов из RDS 2.0 или более поздней части. При использовании DCOM в качестве обычного протокола поддержка RDS 2.0 или более поздней системы более эффективна при транспортировке объектов [Recordset.](recordset-object-ado.md) Если клиент работает с компонентами из RDS 1.5 или ранее, вы можете настроить сервер на работу с предыдущей поддержкой RDS (называемой RDS 1.0) или более новой поддержкой RDS (называемой RDS 2.0 или более поздней). Установите любой из следующих записей реестра:

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-or-

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

