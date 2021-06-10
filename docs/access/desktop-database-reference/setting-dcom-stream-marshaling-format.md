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
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="63715-102">Настройка формата маршалинга потоков DCOM</span><span class="sxs-lookup"><span data-stu-id="63715-102">Setting DCOM stream marshaling format</span></span>


<span data-ttu-id="63715-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63715-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63715-104">Клиентский компьютер, использующий компоненты из RDS 1.5 или ранее, не совместим с сервером с использованием компонентов из RDS 2.0 или более поздней части.</span><span class="sxs-lookup"><span data-stu-id="63715-104">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later.</span></span> <span data-ttu-id="63715-105">При использовании DCOM в качестве обычного протокола поддержка RDS 2.0 или более поздней системы более эффективна при транспортировке объектов [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="63715-105">When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="63715-106">Если клиент работает с компонентами из RDS 1.5 или ранее, вы можете настроить сервер на работу с предыдущей поддержкой RDS (называемой RDS 1.0) или более новой поддержкой RDS (называемой RDS 2.0 или более поздней).</span><span class="sxs-lookup"><span data-stu-id="63715-106">If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later).</span></span> <span data-ttu-id="63715-107">Установите любой из следующих записей реестра:</span><span class="sxs-lookup"><span data-stu-id="63715-107">Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="63715-108">\-or-</span><span class="sxs-lookup"><span data-stu-id="63715-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

