---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dc8644a658b8aca97f80fcf0a942551509064bd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581561"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла. Эта функция принимает в качестве аргументов, в отличие от в формате ANSI этой функции [OpenStreamOnFile](openstreamonfile.md)строки Юникод и таким образом позволяет произвольных символов в поле имя файла, включая расширение файла и путь.
  
|||
|:-----|:-----|
|Экспортировать с:  <br/> |olmapi32.dll  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Параметры

 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _ulFlags_
  
> [in] Битовая маска, флагов, используемых для управления Создание или открытие файла были доступны с помощью объекта OLE **IStream** . Можно задать следующие флажки: 
    
SOF_UNIQUEFILENAME
  
> Временный файл должен быть создан для объекта **IStream** . Если установлен этот флаг, необходимо также задать флаги STGM_CREATE и STGM_READWRITE. 
    
STGM_CREATE
  
> Файл должен быть создан даже в том случае, если он уже существует. Если не задан параметр _lpszFileName_ , как этот флаг, так и в STGM_DELETEONRELEASE должно иметь значение. Если значение STGM_CREATE, необходимо также установить флаг STGM_READWRITE. 
    
STGM_DELETEONRELEASE
  
> Удаление после выхода объекта **IStream** — файл. Если не задан параметр _lpszFileName_ , как этот флаг, так и в STGM_CREATE должно иметь значение. 
    
STGM_READ
  
> Файл является создана или открыта с доступом только для чтения.
    
STGM_READWRITE
  
> Файл является создана или открыта с разрешением на чтение и запись. Если этот флаг не установлен, флаг STGM_CREATE не должно быть задано либо.
    
 _lpszFileName_
  
> [in] Имя файла, включая путь и расширение Юникод с именем файла, для которого **OpenStreamOnFileW** инициализирует объект **IStream** . Если значение флага SOF_UNIQUEFILENAME, _lpszFileName_ содержит путь к каталогу, в котором следует создать временный файл. Если _lpszFileName_ имеет значение NULL, **OpenStreamOnFileW** получает соответствующий путь из системы и должно быть задано как STGM_CREATE, так и STGM_DELETEONRELEASE флаги. 
    
 _lpszPrefix_
  
> [in] Префикс имени файла Юникод, на котором **OpenStreamOnFileW** инициализирует объект **IStream** . Если задано, префикс должен содержать не более трех символов. Если _lpszPrefix_ имеет значение NULL, используется префикс «SOF». 
    
 _lppStream_
  
> [out] Указатель на указатель на объект, предоставление интерфейса **IStream** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_ACCESS
  
> Файл недоступен из-за разрешений недостаточно пользователя или из-за нельзя изменять файлы, доступные только для чтения.
    
MAPI_E_NOT_FOUND
  
> Заданный файл не существует.
    
## <a name="remarks"></a>Замечания

Функция **OpenStreamOnFileW** имеет два важных применения в дополнение к обработке файл с именем Юникод, различающихся по состояние флага SOF_UNIQUEFILENAME. Если этот флаг не задан, **OpenStreamOnFileW** открывает объект **IStream** на существующий файл, например скопировать его содержимое вложения с помощью **со значением свойства **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) IStream::CopyTo** метод. В этом случае параметр _lpszFileName_ указывает путь и имя файла. 
  
Если для SOF_UNIQUEFILENAME, **OpenStreamOnFileW** создает временный файл для хранения данных для объекта **IStream** . Использования этого параметра _lpszFileName_ при необходимости можно указать путь к папке, где он будет создан, а параметр _lpszPrefix_ при необходимости можно указать префикс для имени файла. 
  
По завершении вызывающему приложению клиента или поставщика услуг с объектом **IStream** , его следует освободить путем вызова метода OLE **IStream::Release** . 
  
MAPI с помощью функции, на который указывает _lpAllocateBuffer_ и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, таких как [IMAPIProp:: GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Флаг SOF_UNIQUEFILENAME используется для создания временный файл с именем для системы обмена сообщениями. Если установлен этот флаг указывает параметр _lpszFileName_ путь для временный файл, а параметр _lpszPrefix_ содержит указанные символы префикс имени файла. — Это имя созданного файла <prefix>HHHH. TMP, где HHHH — это шестнадцатеричный номер. Если _lpszFileName_ имеет значение NULL, файл будет создан в каталог временных файлов, который возвращается функцией Windows **GetTempPath**, или в текущем каталоге при назначении не каталог временных файлов.
  
Если флаг SOF_UNIQUEFILENAME не установлен, учитывается, _lpszPrefix_ и _lpszFileName_ должен содержать полный путь и имя файла, который требуется открыть или создать. Файл будет открыт или создан на основании других метки, установленные в _ulFlags_.
  
## <a name="see-also"></a>См. также



[OpenStreamOnFile](openstreamonfile.md)

