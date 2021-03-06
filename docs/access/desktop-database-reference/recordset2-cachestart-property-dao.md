---
title: Свойство Recordset2.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6f68cc9704d7dafe7a1d779b338294c9d5fc1c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307422"
---
# <a name="recordset2cachestart-property-dao"></a>Свойство Recordset2.CacheStart (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое определяет закладку первой записи в объекте Recordset типа dynaset, содержащих данные, локально кэшируемые из источника данных ODBC (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . CacheStart

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Примечания

Кэшинг данных повышает производительность при использовании объектов **Recordset** для получения данных с удаленного сервера. Кэш — это пространство в локальной памяти, которое содержит данные, полученные с сервера; это полезно, если пользователи снова запрашивают данные во время работы приложения. При запросе данных пользователи сначала проверяют кэш для запрашиваемой информации, а не отбирают их с сервера, что занимает больше времени. Кэш сохраняет только данные, которые приходят из источника данных ODBC.

Любой источник данных базы данных Microsoft Access, подключенный к базе данных ODBC, например связанная таблица, может иметь локальный кэш. Чтобы создать кэш, откройте объект **Recordset** из удаленного источника данных, установите свойства **CacheSize** и **[CacheStart,](recordset2-cachestart-property-dao.md)** а затем используйте метод **[FillCache](recordset2-fillcache-method-dao.md)** или перешагите записи с помощью методов **Move.**

Параметр **свойства CacheStart** — это закладки первой записи объекта **Recordset,** который будет кэшироваться. Вы можете использовать закладки любой записи, чтобы установить **свойство CacheStart.** Сделайте запись, которую необходимо запустить кэш текущей записи, и установите свойство **CacheStart,** равное свойству **[Bookmark.](recordset2-bookmark-property-dao.md)**

Двигатель базы данных Microsoft Access запрашивает записи в кэше в диапазоне от кэша, а записи за пределами кэша запрашивает сервер.

Записи, извлеченные из кэша, не отражают изменения, внесенные одновременно с исходными данными других пользователей.

Чтобы принудить к обновлению всех кэшных данных, установите свойство **CacheSize** объекта **Recordset** до 0, повторно установите его до размера первоначально запрашиваемого кэша, а затем используйте метод **FillCache.**

