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
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406026"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла. Эта функция принимает строки UNICODE в качестве аргументов, в отличие от версии ANSI этой функции [OpenStreamOnFile,](openstreamonfile.md)и, таким образом, позволяет использовать произвольные символы в имени файла, включая путь и расширение файла.
  
|||
|:-----|:-----|
|Экспортируемая по:  <br/> |olmapi32.dll  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _ulFlags_
  
> [in] Битмаски флагов, используемых для управления созданием или открытием файла, к нему можно получить доступ через объект OLE **IStream.** Можно установить следующие флаги: 
    
SOF_UNIQUEFILENAME
  
> Для объекта IStream должен быть создан **временный** файл. Если этот флаг заданной, STGM_CREATE и STGM_READWRITE должны быть заданной. 
    
STGM_CREATE
  
> Файл должен быть создан, даже если он уже существует. Если параметр  _lpszFileName_ не задан, необходимо STGM_DELETEONRELEASE этот флаг. Если STGM_CREATE установлено, STGM_READWRITE должен быть также установлен флаг. 
    
STGM_DELETEONRELEASE
  
> Файл должен быть удален после выпуска **объекта IStream.** Если параметр  _lpszFileName_ не задан, необходимо STGM_CREATE этот флаг. 
    
STGM_READ
  
> Файл должен быть создан или открыт с доступом только для чтения.
    
STGM_READWRITE
  
> Файл должен быть создан или открыт с разрешения на чтение и написание. Если этот флаг не установлен, STGM_CREATE не должен быть заданной.
    
 _lpszFileName_
  
> [in] Имя файла, включая путь и расширение, файла с именем Unicode, для которого **OpenStreamOnFileW** инициализирует **объект IStream.** Если флаг SOF_UNIQUEFILENAME,  _lpszFileName_ содержит путь к каталогу, в котором создается временный файл. Если  _lpszFileName_ является NULL, **OpenStreamOnFileW** получает соответствующий путь из системы, и необходимо установить STGM_CREATE и STGM_DELETEONRELEASE флаги. 
    
 _lpszPrefix_
  
> [in] Префикс для имени файла Unicode, на котором **OpenStreamOnFileW** инициализирует **объект IStream.** Если установлено, префикс должен содержать не более трех символов. Если  _lpszPrefix_ является NULL, используется префикс "SOF". 
    
 _lppStream_
  
> [вышел] Указатель на указатель на объект, подвергая обнажаемой **интерфейсу IStream.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_ACCESS
  
> Доступ к файлу был недостаточен из-за недостаточного количества разрешений пользователей или из-за невозможного изменения файлов, доступных только для чтения.
    
MAPI_E_NOT_FOUND
  
> Назначенный файл не существует.
    
## <a name="remarks"></a>Примечания

Функция **OpenStreamOnFileW** имеет два важных использования в дополнение к обработке файла с именем Unicode, отличаемого параметром флага SOF_UNIQUEFILENAME. Если этот флаг не установлен, **OpenStreamOnFileW** открывает объект **IStream** в существующем файле, например для копирования его содержимого в свойство [PR_ATTACH_DATA_BIN (PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)вложения с помощью метода **IStream::CopyTo.**  В этом случае  _параметр lpszFileName_ указывает путь и имя файла файла. 
  
Когда SOF_UNIQUEFILENAME установлено, **OpenStreamOnFileW** создает временный файл для хранения данных для **объекта IStream.** Для этого использования параметр  _lpszFileName_ может необязательно назначать путь к каталогу, в котором должен быть создан файл, а параметр  _lpszPrefix_ может дополнительно указать префикс для имени файла. 
  
После завершения работы клиентского приложения или поставщика услуг с объектом **IStream** необходимо освободить его, позвонив методу OLE **IStream::Release.** 
  
MAPI использует функции, на которые указывают  _lpAllocateBuffer_ и  _lpFreeBuffer_ для большинства распределений памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Флаг SOF_UNIQUEFILENAME используется для создания временного файла с именем, уникальным для системы обмена сообщениями. Если этот флаг задан, параметр  _lpszFileName_ заметив путь для временного файла, а параметр  _lpszPrefix_ содержит символы префикса имени файла. Построенное имя файла — <prefix> это HHHH. TMP, где HHHH — это гексадецимальное число. Если _lpszFileName_ является NULL, файл будет создан во временном каталоге файлов, который возвращается из функции **Windows GetTempPath** или текущего каталога, если не назначен временный каталог файлов.
  
Если флаг SOF_UNIQUEFILENAME не установлен,  _lpszPrefix_ игнорируется, а  _lpszFileName_ должен содержать полностью квалифицированный путь и имя файла для открытия или создания файла. Файл будет открыт или создан на основе других флагов, установленных в  _ulFlags_.
  
## <a name="see-also"></a>См. также



[OpenStreamOnFile](openstreamonfile.md)

