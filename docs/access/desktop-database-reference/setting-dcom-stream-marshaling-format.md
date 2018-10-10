---
title: Setting DCOM Stream Marshaling Format
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0c05a378624f118f1bf6f070273b686a2e50a6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481560"
---
# <a name="setting-dcom-stream-marshaling-format"></a><span data-ttu-id="66cf3-102">Setting DCOM Stream Marshaling Format</span><span class="sxs-lookup"><span data-stu-id="66cf3-102">Setting DCOM Stream Marshaling Format</span></span>


<span data-ttu-id="66cf3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="66cf3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="66cf3-104">Клиентский компьютер с помощью компонентов служб удаленных рабочих СТОЛОВ 1.5 или более ранней версии не совместим с сервером с использованием компонентов служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="66cf3-104">A client computer using components from RDS 1.5 or earlier is not compatible with a server using components from RDS 2.0 or later.</span></span> <span data-ttu-id="66cf3-105">При использовании DCOM протоколе, поддержка для служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии более эффективно с точки зрения переноса объекты [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="66cf3-105">When using DCOM as the underlying protocol, the support for RDS 2.0 or later is more efficient in transporting [Recordset](recordset-object-ado.md) objects.</span></span> <span data-ttu-id="66cf3-106">Если ваш клиент использует компоненты служб удаленных рабочих СТОЛОВ 1.5 или более ранней версии, можно задать сервер для работы с предыдущей Поддержка служб удаленных рабочих СТОЛОВ (называемые служб удаленных рабочих СТОЛОВ 1.0) или более поздней версии поддерживают служб удаленных рабочих СТОЛОВ (называемое служб удаленных рабочих СТОЛОВ 2.0 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="66cf3-106">If your client is running components from RDS 1.5 or earlier, you can set your server to work with the previous RDS support (called RDS 1.0) or the newer RDS support (called RDS 2.0 or later).</span></span> <span data-ttu-id="66cf3-107">Задавайте для следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="66cf3-107">Set either of the following registry entries:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

<span data-ttu-id="66cf3-108">\-или -</span><span class="sxs-lookup"><span data-stu-id="66cf3-108">\-or-</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

