---
title: Свойство QueryDef. CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301094"
---
# <a name="querydefcachesize-property-dao"></a>Свойство QueryDef. CacheSize (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально. Для чтения и записи, **Long**.

## <a name="syntax"></a>Синтаксис

*Expression* . CacheSize

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Значение свойства **CacheSize** должно находиться в пределах от 5 до 1200, но не больше, чем доступная память. Типичное значение — 100. Значение 0 отключает кэширование.

Ядро СУБД Microsoft Access запрашивает записи в диапазоне кэша из кэша и запрашивает записи за пределами диапазона кэша с сервера.

Записи, извлеченные из кэша, не отражают параллельные изменения, внесенные другими пользователями в исходные данные.

