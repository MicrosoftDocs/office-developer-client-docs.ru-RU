---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439095"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла. Эта функция принимает строку ANSI в качестве имени файла, включая путь и расширение файла, поэтому рекомендуется использовать версию Юникод этой функции [OpenStreamOnFileW.](openstreamonfilew.md)
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Параметры

 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, используемых для управления созданием или открытием файла для доступа через объект OLE **IStream.** Можно установить следующие флаги: 
    
SOF_UNIQUEFILENAME 
  
> Для объекта IStream необходимо создать **временный** файл. Если этот флаг установлен, также STGM_CREATE и STGM_READWRITE флаги. 
    
STGM_CREATE 
  
> Файл создается, даже если он уже существует. Если параметр  _lpszFileName_ не задан, необходимо установить и этот STGM_DELETEONRELEASE, и флаг. Если STGM_CREATE установлен, необходимо также STGM_READWRITE флага. 
    
STGM_DELETEONRELEASE 
  
> Файл удаляется при удалении **объекта IStream.** Если параметр  _lpszFileName_ не задан, необходимо установить и этот STGM_CREATE, и флаг. 
    
STGM_READ 
  
> Файл необходимо создать или открыть с доступом только для чтения. 
    
STGM_READWRITE 
  
> Файл необходимо создать или открыть с разрешением на чтение и записи. Если этот флаг не установлен, STGM_CREATE не должен быть установлен. 
    
 _lpszFileName_
  
> [in] Имя файла, включая путь и расширение, для которого **OpenStreamOnFile** инициализирует **объект IStream.** Если установлен SOF_UNIQUEFILENAME,  _lpszFileName_ содержит путь к каталогу, в котором необходимо создать временный файл. Если  _lpszFileName_ имеет NULL, **OpenStreamOnFile** получает соответствующий путь из системы, и необходимо установить STGM_CREATE и STGM_DELETEONRELEASE флаги. 
    
 _lpszPrefix_
  
> [in] Префикс имени файла, по которому **OpenStreamOnFile** инициализирует **объект IStream.** Если этот префикс установлен, он должен содержать не более трех символов. Если  _lpszPrefix_ имеет NULL, используется префикс SOF. 
    
 _lppStream_
  
> [out] Указатель на указатель на объект, который выдает интерфейс **IStream.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_NO_ACCESS 
  
> Не удалось получить доступ к файлу из-за недостаточного количества разрешений пользователя или из-за невозможность изменения файлов, доступных только для чтения. 
    
MAPI_E_NOT_FOUND 
  
> Указанный файл не существует.
    
## <a name="remarks"></a>Примечания

Функция **OpenStreamOnFile** имеет два важных использования, различается по SOF_UNIQUEFILENAME флага. Если этот флаг не установлен, **OpenStreamOnFile** открывает объект **IStream** в существующем файле, например для копирования его содержимого в свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)вложения с помощью метода **IStream::CopyTo.** В этом случае  _параметр lpszFileName_ указывает путь и имя файла. 
  
Когда SOF_UNIQUEFILENAME, **OpenStreamOnFile** создает временный файл для хранения данных для **объекта IStream.** Для этого использования параметр  _lpszFileName_ при желании может указать путь к каталогу, в котором будет создан файл, а параметр  _lpszPrefix_ при желании может указать префикс для имени файла. 
  
После завершения вызова клиентского приложения или поставщика службы с объектом **IStream** он должен освободить его, вызывая метод OLE **IStream::Release.** 
  
MAPI использует функции, на которые указывают  _lpAllocateBuffer_ и  _lpFreeBuffer,_ для выделения большей части памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Флаг SOF_UNIQUEFILENAME используется для создания временного файла с именем, уникальным для системы обмена сообщениями. Если этот флаг установлен, параметр  _lpszFileName_ заносит путь к временному файлу, а параметр  _lpszPrefix_ содержит символы префикса имени файла. Сконструированы имена файлов <prefix> HHHH. TMP, где ЧЧЧ — это деxadecimal number. Если  _lpszFileName_ имеет NULL, файл будет создан во временном каталоге файлов, возвращаемом функцией Windows **GetTempPath,** или в текущем каталоге, если временный каталог файлов не назначен. 
  
Если флаг SOF_UNIQUEFILENAME не установлен,  _lpszPrefix_ игнорируется, а  _lpszFileName_ должен содержать полное имя файла, который необходимо открыть или создать. Файл будет открыт или создан на основе других флагов, установленных в _ulFlags._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI использует метод **OpenStreamOnFile** для открытия потока в файле, чтобы вложение можно было в него записано.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

