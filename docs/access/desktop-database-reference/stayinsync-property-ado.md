---
title: Свойство StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308493"
---
# <a name="stayinsync-property-ado"></a>Свойство StayInSync (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, изменяется ли [](recordset-object-ado.md) ссылка на логичные записи детей (то есть главу) при изменениях позиции родительской строки.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Boolean.** Значение по умолчанию — **True**. Если **true,** глава будет обновлена, если родительский объект **Recordset** меняет позицию строки; если **false,** в главе будут по-прежнему ссылаться на данные в предыдущей главе, даже если родительский объект **Recordset** изменил позицию строки.

## <a name="remarks"></a>Примечания

Это свойство применяется к иерархическим наборам записей, таким как те, которые поддерживаются службой формирования  данных Майкрософт для  [OLE DB,](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)и должно быть установлено в родительском наборе записей перед извлечением детского набора записей. Это свойство упрощает навигацию по иерархическим записям.

