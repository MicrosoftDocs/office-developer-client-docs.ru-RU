---
title: Свойство URL-адрес (RDS - ссылки для настольных баз данных Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479743"
---
# <a name="url-property-rds"></a>URL Property (RDS)


**Применимо к**: Access 2013 | Office 2013



Указывает строку, которая содержит относительный или абсолютный URL-адрес.

Можно задать свойство **URL-адреса** в тег OBJECT объекта [DataControl](datacontrol-object-rds.md) во время разработки или во время выполнения в код сценария.

## <a name="syntax"></a>Синтаксис

Время разработки: \<параметров имя = значение «URL-адрес» = «Сервер»\>

Во время выполнения: DataControl.URL="Server»

## <a name="parameters"></a>Параметры

  - *Сервер*

  - **Строковое** значение, содержащее допустимый URL-адрес.

  - *DataControl*

  - Объектная переменная, которая представляет собой объект- **DataControl** .

## <a name="remarks"></a>Замечания

Как правило URL-адрес указывает файл страницы Active Server (.asp), который может создавать и возвращать [набора записей](recordset-object-ado.md). Таким образом пользователь может получить **записей** без вызова объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или программа настраиваемый бизнес-объект.

Если свойство **URL-адрес** [SubmitChanges](submitchanges-method-rds.md) будет внесения изменений в расположении, указанном URL-адрес.

