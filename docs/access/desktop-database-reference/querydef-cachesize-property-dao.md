---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 827e0c751101ca68246278c04a408731b77c36a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885124"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef.CacheSize Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально. Чтение и запись **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . CacheSize

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Значение свойства **CacheSize** должен быть между 5 и 1200, но не больше, чем объем доступной памяти будет разрешено. Стандартное значение равно 100. Значение 0 отключает кэширование.

Ядро базы данных Microsoft Access запрашивает записей в диапазоне кэша из кэша и запрашивает записи вне диапазона кэша с сервера.

Записей, полученных из кэша не отражает параллельных изменений других пользователей в источник данных.

