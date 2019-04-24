---
title: Свойство ReadyState (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300821"
---
# <a name="readystate-property-rds"></a>Свойство ReadyState (RDS)

**Область применения**: Access 2013, Office 2013

Показывает ход выполнения объекта " [элемент управления](datacontrol-object-rds.md) данными" при извлечении данных в объект [Recordset](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Адкреадистателоадед</strong></p></td>
<td><p>Текущий запрос по-прежнему выполняется, и строки не извлекаются. <strong>Набор записей</strong> объекта " <strong>элемент управления</strong> данных" недоступен для использования.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адкреадистатеинтерактиве</strong></p></td>
<td><p>Начальный набор строк, извлеченный текущим запросом, был сохранен в наборе <strong></strong> <strong>записей</strong> объекта данных и доступен для использования. Остальные строки все еще выбираются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адкреадистатекомплете</strong></p></td>
<td><p>Все строки, извлеченные текущим запросом, были сохранены в <strong></strong> <strong>наборе записей</strong> объекта данных и доступны для использования. Это состояние также будет существовать, если операция прервана из-за ошибки или объект <strong>Recordset</strong> не инициализирован.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять объявления для них. Вы можете вырезать и вставить объявления констант из файла Адквбс. Inc, расположенного в папке C:\Program Files\Common Филес\систем\мсадк.

## <a name="remarks"></a>Замечания

Используйте событие [онреадистатечанже](onreadystatechange-event-rds.md) для отслеживания изменений в свойстве **ReadyState** во время асинхронной операции запроса. Это более эффективно, чем периодическая проверка значения свойства.

Если во время асинхронной операции возникает ошибка, свойство **ReadyState** изменяется на **Адкреадистатекомплете**, свойство [State](state-property-ado.md) изменяется с **адстатиксекутинг** на **адстатеклосед**, а объект **Recordset** Свойство [value](value-property-ado.md) объекта *не*остается.

