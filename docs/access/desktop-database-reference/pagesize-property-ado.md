---
title: Свойство PageSize (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288135"
---
# <a name="pagesize-property-ado"></a>Свойство PageSize (ADO)


**Область применения**: Access 2013, Office 2013

Указывает количество записей, составляющих одну страницу [в Наборе записей.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long,** которое указывает количество записей на странице. По умолчанию используется значение 10.

## <a name="remarks"></a>Примечания

Используйте **свойство PageSize,** чтобы определить, сколько записей составляют логическую страницу данных. Установление размера страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перемещения к первой записи определенной страницы. Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю просматривать данные, просматривая определенное количество записей одновременно.

Это свойство может быть установлено в любое время, и его значение будет использоваться для вычисления расположения первой записи определенной страницы.

