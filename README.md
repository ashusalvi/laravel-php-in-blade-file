# laravel-php-in-blade-file

echo "# laravel-php-in-blade-file" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/ashusalvi/laravel-php-in-blade-file.git
git push -u origin master


code 
							{{--*/ $max_cid= 1 /*--}}
                            @foreach($data as $datavar)
                                @if ($max_cid < $datavar->cid)
                                    {{--*/ $max_cid = $datavar->cid /*--}}
                                @endif
                            @endforeach
                            <option value="{{$max_cid}}" hidden >Choose Cycle</option>
                            @foreach($data as $datavar)
                              <option value="{{$datavar->cid}}" >{{$datavar->productName}}</option>
                            @endforeach
