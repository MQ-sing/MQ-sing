# Example
```C++
import github_file;

struct MQ{
  MQ(MQ&&)=delete("single");
  MQ(const MQ&)=delete("NO CLONE!!!");
  [[noreturn]]std::nullptr_t brain()const{
  /*TODO*/return nullptr;
  };
};

MQ self{};

int main(){
  auto file = githubfile::get("MQ-sing/README.md","w");
  if(!file) return -1;
  auto brain = self.brain();
  file->write(brain->think_for("README.md for myself"));
  return 0;
}
```
Output:
```
Program terminated with signal: SIGSEGV
```
