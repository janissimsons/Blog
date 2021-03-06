[![Build](https://github.com/janissimsons/Blog/actions/workflows/build.yml/badge.svg)](https://github.com/janissimsons/Blog/actions/workflows/build.yml) 
[![Deploy](https://github.com/janissimsons/Blog/actions/workflows/deploy.yml/badge.svg)](https://github.com/janissimsons/Blog/actions/workflows/deploy.yml)

# [ janis writes code ] - coding blog
Source code for [janiswritescode.com](janiswritescode.com)

## Production Release v1
- [x] Production server is setup
- [x] CI/CD pipelines are ready
- [x] Automatic release versioning
- [ ] Cards content stretches entire row's height
- [ ] Article layout fixed
- [ ] Edit card (title, description, image) - tinymce inline editing
- [ ] Feature switch: admin mode
- [ ] Change article visibility. Mark as draft or published  
- [ ] navbar sticky at top  
- [ ] Authentication
- [ ] Code styling is missing for articles

## Backlog  
- [ ] Reading indicator line (scroll and update how much article is left to read)  
- [ ] footer sticky at bottom  
- [ ] TinyMCE needs a separate tab. Like github editor.  
- [ ] Github, gmail integration for comments section
- [ ] Tags, categories
- [ ] Automatic DB backups
- [ ] Save all Linux configs, for disaster recovery
- [ ] About page
- [ ] Footer contains release version
- [ ] Articles which are being edited should auto-save from time to time
- [ ] Access prod db with local editors
- [ ] Image caption styling is missing

## Done
- [x] When resizing browser - logo height must become smaller (along with img)  



EF commands:  
dotnet ef migrations add Init --context Context --startup-project ..\Blog.Web  
dotnet ef database update --context Context --startup-project ..\Blog.Web  
dotnet ef migrations remove --context Context --startup-project ..\Blog.Web  
dotnet ef migrations script --context Context --startup-project ..\Blog.Web  
dotnet publish -c Release -o "prod" --framework net6.0 --runtime linux-x64 /p:EnvironmentName=Production --no-self-contained
