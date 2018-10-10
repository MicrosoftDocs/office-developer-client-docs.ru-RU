---
title: Refresh Method (RDS)
TOCTitle: Refresh Method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d7d1ecb009f61933328695ccbfbea06ac9d7b0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480343"
---
# <a name="refresh-method-rds"></a>Refresh Method (RDS)


**Применимо к**: Access 2013 | Office 2013

Повторный запрос источника данных, указанных в свойстве [подключение](connect-property-rds.md) и обновляет результаты запроса.

## <a name="syntax"></a>Синтаксис

*DataControl*. Обновление

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

## <a name="remarks"></a>Замечания

Прежде чем использовать метод **Refresh** , необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) . Все элементы управления с привязкой к данным на форму, связанную с **RDS. DataControl** объекта будет содержать новый набор записей. Выпущен любого существующего объекта [набора записей](recordset-object-ado.md) и не учитываются несохраненные изменения. Метод **Refresh** автоматически преобразует первую запись текущей записи.

Рекомендуется вызвать метод **Refresh** периодически при работе с данными. Если извлечения данных и оставьте его на клиентском компьютере какое-то время, скорее всего, устаревший. Существует возможность, что все изменения, внесенные завершится с ошибкой, так как другому пользователю, могут измениться эту запись и отправил изменения перед выполнением.

