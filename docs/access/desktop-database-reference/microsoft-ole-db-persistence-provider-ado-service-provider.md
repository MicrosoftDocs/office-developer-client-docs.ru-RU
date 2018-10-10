---
title: Microsoft OLE DB Persistence Provider (ADO Service Provider)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee7f29fa12b7158f2886f908666fa485ddf291cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481206"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Microsoft OLE DB Persistence Provider (ADO Service Provider)


**Применимо к**: Access 2013 | Office 2013 

Поставщик OLE DB сохраняемость позволяет сохранить объект [набора записей](recordset-object-ado.md) в файл и восстанавливать этот объект **набора записей** из файла. Сведения о схеме, данные и ожидающие изменения сохраняются.

**Набор записей** можно сохранить в собственный формат дополнительные данные в таблице грамматики (ADTG) или форматов open языке (XML).

## <a name="provider-keyword"></a>Ключевое слово поставщика

Для вызова этого поставщика, укажите следующие ключевое слово и значение в строке подключения.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Errors

В приложении могут быть обнаружены следующие ошибки, выданный данного поставщика.

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
<td><p>Файл, открытый не имеет допустимый формат (то есть, формат не ADTG или XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>Сохранить объект <strong>набора записей</strong> имеет характеристики, которые запретить сохранение.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Поставщик OLE DB сохраняемость предоставляет не динамические свойства.

В настоящее время невозможно сохранить только параметризованный иерархических объекты **набора записей** .

Дополнительные сведения о постоянно хранение **записей** объектов [Набора записей](more-about-recordset-persistence.md)см.

При использовании потока для открытия **набора записей**должен быть указаны никакие параметры, отличные от *источника* параметра метода **Open** .
