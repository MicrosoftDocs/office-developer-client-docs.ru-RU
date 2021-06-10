---
title: Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288955"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Поставщик услуг хранения Microsoft OLE DB (поставщик служб ADO)


**Область применения**: Access 2013, Office 2013 

Поставщик сохраняемости Microsoft OLE DB позволяет сохранить объект [Recordset](recordset-object-ado.md) в файле, а затем восстановить объект **Recordset** из файла. Сведения о схеме, данные и ожидающих изменений сохраняются.

Можно сохранить набор **записей** либо в фирменом формате Advanced Data Table Gram (ADTG), либо в формате open Extensible Markup Language (XML).

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать этого поставщика, укажите следующее ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Ошибки

Следующие ошибки, выданные этим поставщиком, можно обнаружить в вашем приложении.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>Открытый файл не имеет допустимый формат (то есть формат не ADTG или XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>Сохраненный <strong>объект Recordset</strong> имеет характеристики, которые мешают ему храниться.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Поставщик сохраняемости Microsoft OLE DB не предоставляет динамические свойства.

В настоящее время невозможно сохранить только параметризированные объекты **иерархического набора** записей.

Дополнительные сведения о постоянном хранении объектов **Recordset** см. в дополнительных [сведениях о сохраняемом сохраняемом наборе данных.](more-about-recordset-persistence.md)

Когда поток используется для открытия **наборов записей,** не должно быть параметров, заданных, кроме *параметра Source* метода **Open.**

