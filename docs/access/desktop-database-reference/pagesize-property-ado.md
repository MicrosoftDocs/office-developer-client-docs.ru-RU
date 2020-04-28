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

Указывает, сколько записей составляют одну страницу в [наборе записей](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** , которое указывает количество записей на странице. По умолчанию используется значение 10.

## <a name="remarks"></a>Примечания

Используйте свойство **pageSize** , чтобы определить, сколько записей составляют логическую страницу данных. Установка размера страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы. Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю просматривать данные, одновременно просматривая определенное количество записей.

Это свойство можно задать в любое время, и его значение будет использоваться для вычисления расположения первой записи определенной страницы.

