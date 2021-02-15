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

Поставщик сохраняемости Microsoft OLE DB позволяет сохранить объект [Recordset](recordset-object-ado.md) в файле, а затем восстановить этот объект **Recordset** из файла. Сведения о схеме, данные и ожидающих изменений сохраняются.

Набор записей  можно сохранить либо в проприетарном формате ADTG, либо в открытом формате XML.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать этого поставщика, укажите следующее ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Ошибки

В приложении могут быть обнаружены следующие ошибки, выданные этим поставщиком.

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
<td><p>Открытый файл не имеет допустимый формат (т. е. формат не ADTG или XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>Сохраненный <strong>объект Recordset</strong> имеет характеристики, которые не могут его сохранить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Поставщик сохраняемости Microsoft OLE DB не предоставляет динамические свойства.

В настоящее время нельзя сохранить только параметризованные иерархические объекты **recordset.**

Дополнительные сведения о постоянном хранении объектов **Recordset** см. в [записях сохраняемости.](more-about-recordset-persistence.md)

Если поток используется для открытия **recordset,** параметры, кроме параметра *Source* метода Open, не должны **быть указаны.**

