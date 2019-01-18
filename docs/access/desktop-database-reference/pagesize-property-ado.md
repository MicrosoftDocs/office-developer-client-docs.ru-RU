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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709553"
---
# <a name="pagesize-property-ado"></a>Свойство PageSize (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, сколько записей составляют одну страницу в [набора записей](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , указывающее количество записей на странице. Значение по умолчанию — 10.

## <a name="remarks"></a>Замечания

Свойство **PageSize** используется для определения числа записей, входящих в состав логической страницы данных. Создание размер страницы позволяет использовать свойство [AbsolutePage](absolutepage-property-ado.md) для перехода к первой записи определенной страницы. Это полезно в сценариях веб-сервера, когда необходимо разрешить пользователю страницу с помощью данных, просмотр нескольких записей одновременно.

Это свойство можно задать в любое время и его значение будет использоваться для расчета местоположение первой записи определенной страницы.

